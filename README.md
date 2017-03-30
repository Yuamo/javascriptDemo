# javascriptDemo




```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<script>
			let date = new Date();
			// 时间复制
			let d = new Date(date);
			let arr = [];
			arr.push(date.getFullYear());
			arr.push((date.getMonth()+1)>10?(date.getMonth()+1):'0'+(date.getMonth()+1));
			arr.push(date.getDate()>10?date.getDate():'0'+date.getDate());
			let week = ['日','一','二','三','四','五','六'];
			arr.push('星期'+week[date.getDay()]);
			let h = date.getHours();
			arr.push(h>12?'下午':'上午');
			// 时间如果大于12 就会断路后面的不执行
			h>12&&(h-=12)
			arr.push(h>10?h:'0'+h);			
			arr.push(date.getMinutes()>10?date.getMinutes():'0'+date.getMinutes());
			arr.push(date.getSeconds())
			let str= arr.join('')
			// 20170329星期三下午082826
			let reg = /(\d{4})(\d{2})(\d{2})星期([日一-六])([上下]午)(\d{2})(\d{2})(\d{2})/;
			str = str.replace(reg,'$1年$2月$3日   星期$4  $5  $6:$7:$8')
			console.log(str);
			
		</script>
	</body>
</html>
```
