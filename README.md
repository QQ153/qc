数组去重
可以这样试下
		
		Array.prototype.unique = function(){
			var n ={} ,r = [];
			for(var i=0;i<this.length;i++){
				if(!n[this[i]]){
					n[this[i]]=true;
					r.push(this[i]);
				}
			}
			return r;
		}
		
		
		Array.prototype.unique2 = function(){
			this.sort();
			var biao = [this[0]];
			for(var i = 1;i<this.length;i++){
				if(this[i]!==biao[biao.length-1]){
					biao.push(this[i]);
				}
			}
			return biao;
		}
