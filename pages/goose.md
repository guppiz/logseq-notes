- **config**
  ~/.config/goose/config.yaml
- **global .goosehints**
  ~/.config/goose/.goosehints
- **logs**
	- Event logs (được in ra khi chạy lệnh CLI) nằm ở thư mục `~/.local/share/goose/sessions/`.[1](https://github.com/block/goose/issues/2078)
	- “Real logs” (log chi tiết hơn) được đề cập là nằm dưới `~/.local/state/goose/logs/` (ví dụ: `~/.local/state/goose/logs/cli/...`).
	- Với Goose Desktop trên macOS, có đề cập tới thư mục log server tại `~/.local/state/goose/logs/server`.[2](https://github.com/block/goose/issues/5636)