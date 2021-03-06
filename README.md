## 代码格式

保证代码质量是团队管理中比较重要的一部分，多人维护的代码保持一样的格式，不仅自己看着舒服，也便于别人维护。以前总没有下定决心去整这一块，这周终于找到一个比较完整的时间，好好跑了下 ESlint 。
第一次跑时，瞬间几千个出现错误和提示，看到这么多问题，几次都想放弃，但是想以后再也不要麻烦了，就一步步走过来了。

在这过程中使用了很多工具，也对前端代码质量管理工具有了较深入的了解。

    1. 为了检测 `JavaScript` 质量，加入了 `eslint`；
    2. 为了检测 `CSS（LESS）`质量，使用了 `stylelint`；
    3. 扫描出来几千个 `error` 之后，使用 `eslint` 的 `--fix` 进行了修复，但是并不是每个都能修复；
    4. 为了快速修复有问题的代码，在 `VSCode` 里面加入了 `Prettier - JavaScript formatter`，配置下VS Code 的`settings.json` 就可以直接在保存的时候，就可以自动自动化代码格式；
    5. 为保证每次书写代码的时候，出现格式错误有提示，在 `VSCode` 加入了 `ESLint` 来检测 `JavaScript`, 加入 `stylelint` 来检测 `LESS`;
    6. 为了保证代码提交到代码库是规范的，在提交 `git commit` 时，通过 `husky` 提供 `precommit` 方法，在`commit`之前进行代码检测。

下面对以上运用的一些工具进行一些简短的介绍：

## 工具

### JS 代码检测 [ESLint](http://eslint.org)

-   错误级别

> -   'off' 或 0 - 关闭规则
> -   'warn' 或 1 - 开启规则，使用警告级别的错误：warn (不会导致程序退出),
> -   'error' 或 2 - 开启规则，使用错误级别的错误：error (当被触发的时候，程序会退出)

-   [babel-eslint](https://github.com/babel/babel-eslint)
-   [eslint-plugin-react](https://github.com/yannickcr/eslint-plugin-react)

### CSS 代码检测 [StyleLint](https://github.com/stylelint/stylelint)

### 代码格式化工具 [Prettier](https://github.com/prettier/prettier)

### 配置 Git commit/push 之前检测代码 [husky](https://github.com/typicode/husky)


### [editorconfig](https://github.com/editorconfig)

## 配置文件

### [.eslintrc.js](./.eslintrc.js)

### [.stylelintrc.js](./.stylelintrc.js)

### [.editorconfig](./.editorconfig)

### [VScode setting.json](./.vscode/settings.json)
