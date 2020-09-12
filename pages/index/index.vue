<template>
	<view class="content">
		<view style="width: 100%;">
		        <view class="bg-mask " style="top: 0;"></view>
		        <view class="m-share-top">
		            <!--<span class="icon-close"></span>-->
		        </view>
		        <view class="m-register-form">
		            <view class="register-form-box">
		                <view class="register-form-cell">
		
		                    <view class="form-cell-left">
		                        <input class="form-cell-ipt" id="inputTel" type="tel" maxlength="11" onblur="blur()"
		                               oninput="value=value.replace(/[^\d]/g,'')"
		                               placeholder="请输入手机号码"
		                               v-model="info.userName" style="width: 100%;"/>
		                    </view>
		                    <view class="form-cell-right" @click="info.userName=''">
		                        <span class="form-cell-close"></span>
		                    </view>
		                </view>
		                <view class="register-form-cell" style="margin-top: 20px;">
		                    <view class="form-cell-left">
		                        <input class="form-cell-ipt" type="tel" id="inputCode" maxlength="6"
		                               oninput="value=value.replace(/[^\d]/g,'')"
		                               placeholder="请输入密码" v-model="info.code" style="width: 100%;">
		                    </view>
		                </view>
						
		                <view class="register-form-login" style="background: #00b31a;margin-top: 20px;" id="register" @click="register">注册</view>
		            </view>
		            <view style="display: flex;justify-content: center;margin-top: 30px;margin-bottom: 50px">
		                <span class="agreement-txt">注册即同意<a :href="`${link}service-term`" style="color: #00b31a">《用户服务协议》</a></span>
		            </view>
		        </view>
		    </view>
			
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: {
					userName: '',
					code: '',
					userId: '',
					invitationCode: ''
				},
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}
	.register-form-login {
		display: block;
		width: 100%;
		height: 1.173333rem;
		line-height: 1.173333rem;
		font-size: .426667rem;
		text-align: center;
		border-radius: 1.653333rem;
		background: #f1735f;
		color: #fff;
	}
	.invite-register {
	        position: relative;
	    }
	.register-form-cell {
		position: relative;
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-orient: horizontal;
		-webkit-box-direction: normal;
		-ms-flex-direction: row;
		flex-direction: row;
		-webkit-box-align: center;
		-ms-flex-align: center;
		align-items: center;
		height: 1.173333rem;
		padding: 0 0.4rem;
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
		border: 1PX solid #e4e4e4;
		border-radius: 1.653333rem;
		margin-bottom: 0.453333rem;
		background-color: #fff;
	}
	.m-share-top {	
	    width: 100%;
	    height: 360px;
	    background: url(../../static/login.png) no-repeat 50%;
	    background-size: cover;
	}
	.m-register-form {
	    position: relative;
	    top: 30px;
	    width: 100%;
	}
	.register-form-box {
	    width: 80%;
	    margin: 0 auto;
	}
	.register-form-cell {
	    position: relative;
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: flex;
	    -webkit-box-orient: horizontal;
	    -webkit-box-direction: normal;
	    -ms-flex-direction: row;
	    flex-direction: row;
	    -webkit-box-align: center;
	    -ms-flex-align: center;
	    align-items: center;
	    height: 1.8rem;
	    padding: 0 .4rem;
	    box-sizing: border-box;
	    border: 1px solid #e4e4e4;
	    border-radius: 1.653333rem;
	    margin-bottom: .453333rem;
	    background-color: #fff;
	}
	.register-form-login {
	    display: block;
	    width: 100%;
	    height: 1.8rem;
	    line-height: 2rem;
	    font-size: 15px;
	    text-align: center;
	    border-radius: 1.653333rem;
	    background: #f1735f;
	    color: #fff;
	}
	.agreement-txt {
	    font-size: 14px;
	    color: #666;
	}
	.form-cell-close {
	    display: inline-block;
	    width: 18px;
	    height: 18px;
	    background: url(../../static/close-gray.png) no-repeat 50%;
	    background-size: 100%;
	    position: relative;
	    top: .053333rem;
	}
	.form-cell-left {
		display: flex;
		flex: 1;
	}
</style>
