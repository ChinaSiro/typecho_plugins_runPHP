# typecho_plugins_runPHP
typecho1.0插件：在文章内运行php
作者：ChinaSiro
博客：http://hedanku.com

# 使用方法
1.将runPHP目录放到plugins目录中
2.在需要调用的地方插入“调用代码”
3.在后台启用插件并设置好php文件统一的目录
4.发布时，添加runPHP字段，填写php文件名即可
5.在模版function.php中添加“字段代码”可省去上一步

# 调用代码
- 在需要调用的模版位置中插入
<?php runPHP_Plugin::run($this->fields->runPHP);?>

# 字段代码
- 在模版function.php中添加
function themeFields(Typecho_Widget_Helper_Layout $layout){
    $runPHP = new Typecho_Widget_Helper_Form_Element_Text('runPHP', NULL, NULL, _t('runPHP'), _t('要运行的php文件'));
    $layout->addItem($runPHP);
}
