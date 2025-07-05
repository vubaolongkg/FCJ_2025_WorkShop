---
title : "Thiết bị MFA cứng"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

**Nội dung**

- [Kích hoạt thiết bị MFA phần cứng khác thông qua Console](#kích-hoạt-thiết-bị-mfa-phần-cứng-khác-thông-qua-console)

#### Kích hoạt thiết bị MFA phần cứng khác thông qua Console

1. Đăng nhập vào AWS Console.
2. Góc trên bên phải, bạn sẽ thấy tên account của bạn, chọn vào và chọn **My Security Credentials** sau đó mở rộng Multi-factor authentication (MFA).

![Image](/images/1-account-setup/MySecurity_v1.png?width=15pc)

3. Để quản lí khóa bảo mật U2F, bạn phải có quyền từ bộ quyền sau. ở thanh bên trái, chọn **Policies** sau đó chọn **Create policy**, chọn **JSON** tab và dán phần bên dưới vào:

```js
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllowManageOwnUserMFA",
            "Effect": "Allow",
            "Action": [
                "iam:DeactivateMFADevice",
                "iam:EnableMFADevice",
                "iam:GetUser",
                "iam:ListMFADevices",
                "iam:ResyncMFADevice"
            ],
            "Resource": "arn:aws:iam::*:user/${aws:username}"
        },
        {
            "Sid": "DenyAllExceptListedIfNoMFA",
            "Effect": "Deny",
            "NotAction": [
                "iam:EnableMFADevice",
                "iam:GetUser",
                "iam:ListMFADevices",
                "iam:ResyncMFADevice"
            ],
            "Resource": "arn:aws:iam::*:user/${aws:username}",
            "Condition": {
                "BoolIfExists": {
                    "aws:MultiFactorAuthPresent": "false"
                }
            }
        }
    ]
}
```
![MFA](/images/3/0001.png?featherlight=false&width=90pc)

4. Chọn **Next: Tags**. Đây là màn hình về **Tags** một công cụ dùng để phân biệt các tài nguyên của AWS.
5. Chọn  **Next: Review**. Đây là màn hình cho phép bạn review về bộ quyền mà bạn đang tạo ra. 
6. Nhập tên bộ quyền (ví dụ: MFAHardDevice) và chọn **Create policy**.

![MFA](/images/3/0002.png?featherlight=false&width=90pc)

![MFA](/images/3/0003.png?featherlight=false&width=90pc)

7. Ở thanh bên trái , chọn **Dashboard** và sau đó chọn **Enable MFA**.

![MFA](/images/3/0004.png?featherlight=false&width=90pc)

8. Mở rộng Multi-factor authentication (MFA) sau đó chọn **Active MFA**.

9. Trong **Manage MFA Device**, chọn **Other Hardware MFA Device** sau đó nhấn **Continue**.
10. Nhập **Serial Number** ở đằng sau thiết bị.

![Image](/images/1-account-setup/HardwareMFA.png?featherlight=false&width=90pc)

11. Nhập MFA code 1 sau đó đợi 30 giây và nhập MFA code 2.
12. Chọn **Assign MFA**.
