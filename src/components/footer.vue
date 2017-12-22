<template>
    <div class="vfooter">
    	<router-link to="/home" tag="div" class="item">
    		<i class="icon_qa"></i>
    		<span>
    			问答
    		</span>
    	</router-link>
        <div class="item">
            <i class="icon_headline"></i>
            <span>
                头条
            </span>
        </div>
    	<router-link :to="{path: '/message'}" tag="div" class="item">
    		<i class="icon_pencil_square"></i>
    		<span>
    			专栏
    		</span>
    	</router-link>
    	<router-link :to="{path: '/me'}" tag="div" class="item">
    		<i class="icon_play_circle"></i>
    		<span>
    			讲堂 
    		</span>
    	</router-link>
        <div class="item">
            <i class="icon_user_circle"></i>
            <span>
                我的
            </span>
        </div>
    </div>
</template>

<script>
export default{
  name: 'vfooter'
}
</script>

<style rel="stylesheet" scoped lang="less">
@import '~assets/css/varable.less';
.vfooter{
	position:fixed;
    bottom:0;
    left:0;
    right:0;
    height:100px;
    line-height: 100px;
    background-color: #fff;
    box-shadow: 0 -3px 6px rgba(0, 0, 0, 0.06);
    display: flex;
	align-items:center;
	justify-content: space-between;
	text-align: center;
	font-size: 26px;
    .item{
    	flex:1;
    	height:100px;
        color: #9e9e9e;
    	i,span{
    		display: block;
            line-height: 40px;
            text-align: center;
    	}
    	i{
    		width: 34px;
    		height: 34px;
    		margin: 0 auto;
    		margin-top: 18px;
    		display: block;
    		background-repeat: no-repeat;
    		background-size: cover;
    		background-position: center;
    		&.icon_qa{
    			background-image: url('~@/assets/images/qa.svg')
    		}
            &.icon_headline{
                background-image: url('~@/assets/images/headline.svg')
            }
            &.icon_pencil_square{
                background-image: url('~@/assets/images/pencil_square.svg')
            }
            &.icon_play_circle{
                background-image: url('~@/assets/images/play_circle.svg')
            }
            &.icon_user_circle{
                background-image: url('~@/assets/images/user_circle.svg');
            }
    		&.icon_me{
    			background-image: url('~@/assets/images/me.svg');
    		}
    	}
        &.router-link-active{
            color:@color_body_background; 
            .icon_qa{
                background-image: url('~@/assets/images/qa_active.svg')
            }
            .icon_headline{
                background-image: url('~@/assets/images/headline_active.svg')
            }
            .icon_pencil_square{
                background-image: url('~@/assets/images/pencil_square_active.svg')
            }
            .icon_play_circle{
                background-image: url('~@/assets/images/play_circle_active.svg')
            }
            .icon_user_circle{
                background-image: url('~@/assets/images/user_circle_active.svg');
            }
        }
    }
}
    
</style>