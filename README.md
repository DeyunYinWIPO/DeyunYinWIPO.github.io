Jekyll利用编写好的Markdown生成HTML文件。GitHub自带Jekyll，所以项目文件可以直接托管给GitHub，无需自己再建站部署。

# 部署

整个项目clone到自己新建的GitHub库中，库名改成[GitHub名].github.io，_config.yml文件中的url也改成[GitHub名].github.io

<img src="/images/image-20241123205712940.png" alt="image-20241123205712940" style="zoom:50%;" />

# 基础删改

- 模板官方说明 https://academicpages.github.io/

- 基本信息修改：编辑配置文件_config.yml

  <img src="/images/image-20241123200356687.png" alt="image-20241123200356687" style="zoom: 50%;" />

  <img src="/images/{65F5F599-77A2-4AB5-A818-9D45EAB7A4C2}.png" alt="{65F5F599-77A2-4AB5-A818-9D45EAB7A4C2}" style="zoom:50%;" />



- 静态文件（pdf文件等）: /files/
- 主页图片（可以在_config.yml中修改）: images/profile.png

- 顶部导航栏配置：_data/navigation.yml

  ![{39BC5255-2FA8-41DE-A3E3-970B6ACD654B}](../../../BackendDev/TextFolder/SelfStudy/图片库/{39BC5255-2FA8-41DE-A3E3-970B6ACD654B}-1732367447941-3.png)

  <img src="/images/{2BDFBE00-C914-4BF7-8488-BEBEC887392B}.png" alt="{2BDFBE00-C914-4BF7-8488-BEBEC887392B}" style="zoom:50%;" />

  

- **关键*** 编辑导航栏每一项对应的单页：_pages/

  - 每一个单页对应一个markdown文件或html文件。

  - 无论是markdown文件还是html文件，都要编写文件最开头的YAML front matter信息。以Publications栏的publications2.md为例：

    ![{80E04722-2A81-4B88-BA54-F93CDC158488}](/images/{80E04722-2A81-4B88-BA54-F93CDC158488}.png)

    - 在_pages文件夹创建的markdown文件，其名称通常与navigation.yml文件中相应栏目的url一致，方便查找修改，比如此处的publications2.md就与Publications栏的url一致。

      <img src="/images/{AA48D626-C8B3-4BBA-845F-9622C8F43B9A}.png" alt="{AA48D626-C8B3-4BBA-845F-9622C8F43B9A}" style="zoom: 80%;" />

    - `permalink:` 指定页面的永久链接，此处设为`/publications2/`，与navigation.yml文件中Publications栏的url一致
      - 如果设定为/，表示将当前文件映射至网站首页，本项目中的about.md文件是这样配置的。
    - `title:` 设定页面标题，通常会显示在网页的浏览器标签中或页面的显著位置。
      
      - ![image-20241123202306851](/images/image-20241123202306851.png)
    - `redirect_from: `设置重定向路径，可以让其他链接自动跳转到此页面。路径 `/publications2/` 和 `/publications2.html` 将自动跳转到当前页面。**路径名通常与`permalink:` 保持一致。**



- 关于非导航栏页面的相互跳转。一个简单的实现思路是，把所有页面以md的形式写好、YAML front matter信息配置好，放到_pages中，然后把目标页面的路径链接到其他页面中。 比如中文页最底部的test演示





















