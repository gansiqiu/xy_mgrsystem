<template lang="html">
  	<div class="articleAlter">
		<Breadcrumb>
  			<BreadcrumbItem to="/articleManage">
  				<Icon type="ios-build" size="24"/>好文管理
  			</BreadcrumbItem>
			<BreadcrumbItem>
  				<Icon type="md-add" size="24"/>新建好文
  			</BreadcrumbItem>
  		</Breadcrumb><br />
		<Form :model="formItem" :label-width="150">
		   	<FormItem label="好文文章名:">
			   	<Input v-model="formItem.articleName" placeholder="请输入文章名" clearable></Input>
		   	</FormItem>
			<FormItem label="文章类型:">
	            <Select v-model="formItem.articleType" placeholder="选择类型">
	                <Option value="1">New York</Option>
	                <Option value="2">London</Option>
	                <Option value="3">Sydney</Option>
	            </Select>
	        </FormItem>
			<FormItem>
				<Button type="primary" long @click="submitClick">提交</Button>
			</FormItem>
		</Form>
  	</div>
</template>

<script>
export default {
	name:"articleAlter",
	data(){
		return{
			formItem:{
				articleName:"",
				articleType:"1"
			}
		}
	},
	methods:{
		submitClick(){
			console.log("submit");
		}
	}
}
</script>

<style lang="css">
.articleAlter{
	padding: 20px;
}
form{
	width: 70%;
	margin: 0 auto;
}
</style>
