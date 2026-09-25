# hello-go-releases

[![Go CI/CD](https://github.com/Evgeny65ok/hello-go-releases/actions/workflows/ci.yml/badge.svg)](https://github.com/Evgeny65ok/hello-go-releases/actions/workflows/ci.yml)

Учебный проект: **CI/CD на Go** с публикацией бинарников под 5 платформ в **GitHub Releases**.

## Что делает пайплайн
* **Проверки**: `gofmt -l`, `go vet ./...`, `go test ./... -v`
* **Матричная сборка**: параллельная компиляция под `linux/amd64`, `linux/arm64`, `darwin/amd64`, `darwin/arm64`, `windows/amd64`
* **Публикация**: создание релиза в GitHub Release при push тега `v*`
* **Кастомизация**: версия динамически вшивается через `-ldflags "-X main.version=..."`

## Скриншоты

### Actions
<img width="1768" height="618" alt="Снимок экрана 2026-09-25 094317" src="https://github.com/user-attachments/assets/cab93fbd-e94f-4f42-9bd9-11c5414fbddb" />


### Release v1.0.0

<img width="1574" height="916" alt="Снимок экрана 2026-09-25 094350" src="https://github.com/user-attachments/assets/f833c78f-9142-4bdf-8b37-46d172cbe7eb" />

## Использование
Скачайте бинарный файл под вашу платформу со страницы [Releases](../../releases).

### Запуск в Linux / macOS:
```bash
chmod +x hello-go-linux-amd64
./hello-go-linux-amd64
```
<img width="1082" height="668" alt="image" src="https://github.com/user-attachments/assets/146ad5e5-a179-478a-871e-1a301481de84" />

### Вывод программы:
```text
hello-go version v1.0.0
Hello from Go! 🐹
OS: linux
Arch: amd64
Hello, GitHub!
Sum 1..10 = 55
```

## Новый релиз
```bash
git tag v1.1.0
git push origin v1.1.0
```
