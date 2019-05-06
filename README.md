# javascript
> 构造函数和原型对象封装
```
<script type="text/javascript">
		//构造函数
		function Methods() {
		}

		//原型随机数方法
		Methods.prototype.maxrandom=function(){
			return function(max,min){
				return Math.floor(Math.random()*(max-min)+min)
			}
		}

		//原型随机颜色方法
		Methods.prototype.colors=function(){
			var that = this;
			return function(){
				let r =  that.maxrandom()(255,0);
				let g =  that.maxrandom()(255,0);
				let b =  that.maxrandom()(255,0);
				return "rgb("+r+','+g+','+b+")";
			}
		}

		//实例对象
		let myinit = new Methods();
		
		console.log(myinit.maxrandom()(100,1));
		console.log(myinit.colors()())
	</script>

```



> 是否微信qq打开

```
 is_weixn_qq(){
        var ua = navigator.userAgent.toLowerCase();
        //如果是微信和QQ隐藏内容
        if(ua.match(/MicroMessenger\/[0-9]/i)||ua.match(/QQ\/[0-9]/i)){
           this.iswx=true;
           this.tgqd='0';
           return
        }else{
            //如果不是微信和Qq计算pv
            this.init()
        }
    }
```



