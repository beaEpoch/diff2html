# diff2html
将diff -ru 或git diff 的输出转换为html页面，以table格式的side-by-side样式展现

用法：

    diff -ru file1 file2 > diff.out
    作为模块引入
        import diff2html
        txt = subprocess.check_output(['cat','diff.out'])
        diff.table = diff2html.parse_from_memory(txt, True)

jQuery设置折叠效果

$(".diffmisc").click(function(){
        $(this).children("table").toggle();
});
