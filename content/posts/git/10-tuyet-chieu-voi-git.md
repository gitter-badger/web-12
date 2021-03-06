---
layout: post.njk
title: Tăng hiệu suất sử dụng git với git alias
slug: tang-hieu-suat-su-dung-git-voi-git-alias
date: 2017-10-04
tags: git, Tuyệt chiêu, Thủ thuật
cover: https://res.cloudinary.com/hikerlust/image/upload/v1507656024/branching-illustration_2x_r5eddp.png
excerpt: Tiết kiệm thời gian gõ những câu lệnh git dài ngoằng với `git alias`. Đặc biệt, bạn bỗng nhiên trở nên chuyên nghiệp hơn trong mắt đồng nghiệp.
author: kcjpop
---

 `git alias` cho phép bạn đặt tên thay thế cho các câu lệnh thường dùng. Thay vì phải gõ dài dòng như `git commit --amend -s` bạn có thể dùng `git config --global alias.cmsa "commit --amend -s"`, và bùm từ nay chỉ cần `git cmsa` là xong.

Dưới đây là một số alias mình thường dùng

```bash
git config --global alias.a "add"
# Đánh dấu tất cả tập tin trong thư mục hiện tại, chuẩn bị commit
git config --global alias.aa "add . -A"

git config --global alias.c "commit"
# Commit và đặt chữ ký
git config --global alias.cms "commit -s"
# Kết hợp với commit trước đó và đặt chữ ký
git config --global alias.ca "commit --amend -s"

git config --global alias.d "diff"
git config --global alias.ds "diff --stat"
# Hiển thị thay đổi với những tập tin đã được staged
git config --global alias.dc "diff --cached"

git config --global alias.s "status -s"
git config --global alias.co "checkout"
# Checkout  một nhánh mới
git config --global alias.cob "checkout -b"
```

Mình đặc biệt thích `git lg` như dưới đây:

```bash
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```
Với `git log` bình thường, bạn sẽ có lịch sử như hình bên trái, nhưng với `git lg` các commit được gom lại và hiển thị theo dạng đồ thị. Dễ nhìn hơn nhiều.

![](https://res.cloudinary.com/hikerlust/image/upload/v1507655532/AuYbIc3_o4iwfm.png)

Bạn có thể xem thêm các aliases khác ở [GitAlias/gitalias](https://github.com/GitAlias/gitalias). À đừng quên `git yolo`.

![](https://res.cloudinary.com/hikerlust/image/upload/v1507655527/YOLO_v19b1b.png)
