# shortstudio-media — temporary public media host for publishing uploads

Zernio/Composio không tải được media từ Paperclip attachment (auth-gated), nên lúc
publish: đẩy MP4 lên 1 release public ở repo này (`gh release create <tag> file.mp4`),
lấy URL `releases/download/<tag>/<file>` làm `media_urls` cho `ZERNIO_MCP_POSTS_CREATE`.

**Cleanup bắt buộc sau khi post được verify `published`:** `gh release delete <tag> --yes`.
File media KHÔNG nằm trong nội dung repo — chỉ là release asset tạm, xoá sau đăng.
