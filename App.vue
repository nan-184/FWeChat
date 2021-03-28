<script>
	export default {
		
		created: function() {
			// #ifdef APP-PLUS-NVUE
			// 加载公共图标库
			const domModule = weex.requireModule('dom')
			domModule.addRule('fontFace', {
			    'fontFamily': "iconfont",
			    'src': "url('http://at.alicdn.com/t/font_2430317_7n94mntu1z2.ttf')"
			 });
			 // #endif
			 console.log('App Launch');
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	/* #ifndef APP-PLUS-NVUE */
	@import "/static/iconfont/iconfont.css";
	 /* #endif */
</style>
