##jquery中如何实现标签切换效果##

核心代码：

    <!DOCTYPE html>
	<html lang="en">
	<head>
		<meta charset="UTF-8">
		<title>tab</title>
	
	</head>
	<body>
		<ul class="tab">
			<li class="active" data-title="d1">1</li>
			<li data-title="d2">2</li>
			<li data-title="d3">3</li>
		</ul>
		<div class="content">
			<div id="d1">1111</div>
			<div id="d2" style="display:none">2222</div>
			<div id="d3" style="display:none">3333</div>
			<div id="d4" style="display:none">4444</div>
		</div>
	<script src="jquery.js"></script>	
	<script>
		$('ul > li').click(tab);
		function tab() {
			$(this).addClass('active').siblings().removeClass('active');
			var tab = $(this).attr('title');
			$('#'+tab).show().siblings().hide();
		}
	</script>
	</body>
	</html>