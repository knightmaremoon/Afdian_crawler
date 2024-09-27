# AFDian Crawler

This Python script is designed to log in to AFDian, fetch posts from a specified album of a given author, and save the content as markdown (.md) files.

## Prerequisites

1. Install the required Python libraries:
   ```bash
   pip install requests html2text
2. Make sure you have your `cellphone` and `password` ready for AFDian login.

## Parameters
Before running the script, you need to fill in the following parameters:

`cellphone` - Your AFDian account phone number.

`passwd` - Your AFDian account password.

`target_user_id` - The user ID of the author from which you want to fetch the albums.

`album_id` - The album ID that you want to fetch posts from.

# TODO

1. **Fetch all album IDs for a given author in one go**  
   - Use the `fetch_all_albums(user_id)` function to get all the album IDs associated with a specific author.
   - Store these album IDs in a list for further processing.

2. **Create a separate folder for each album ID**  
   - For each album ID retrieved, create a separate folder to store the corresponding posts.
   - Use the `os.mkdir()` function to create directories dynamically based on the album ID.
   - Save the posts of each album in their respective folders in `.md` format.

# Explanation

- **Content Availability and Subscription Restrictions:**  
  The script can only fetch content for posts that are accessible based on the user's account permissions. For example, if the account has not subscribed to a particular tier or content, the script will not be able to fetch the content of those posts. In such cases, while the script will still create files for these posts, the files will be empty.


  # AFDian Crawler

该Python脚本旨在登录AFDian，获取指定作者某个专辑下的文章，并将内容保存为markdown (.md)文件。

## 先决条件

1. 安装所需的Python库：
   ```bash
   pip install requests html2text
    ```
2. 确保您已准备好AFDian的`cellphone`和`password`用于登录。

## 参数
在运行脚本之前，您需要填写以下参数：

`cellphone` - 您的AFDian账户电话号码。

`passwd` - 您的AFDian账户密码。

`target_user_id` - 您想要获取专辑的作者的用户ID。

`album_id` - 您想要抓取文章的专辑ID。

# TODO
1. **一次性抓取指定作者的所有专辑ID**
    使用fetch_all_albums(user_id)函数获取与指定作者相关的所有专辑ID。
    将这些专辑ID存储在一个列表中以便进一步处理。
    为每个专辑ID单独建立文件夹

2. **对于每个获取的专辑ID，创建一个单独的文件夹来存储相应的文章。**
    使用os.mkdir()函数根据专辑ID动态创建文件夹。
    将每个专辑的文章保存到各自的文件夹中，文件格式为.md。

# 补充说明
- **内容可用性与订阅限制：**
该脚本只能抓取基于用户账户权限可以访问的文章内容。例如，如果账户未订阅某个等级或内容，那么该脚本将无法抓取这些文章的内容。在这种情况下，脚本仍会为这些文章创建文件，但文件内容将为空。