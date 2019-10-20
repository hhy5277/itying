https://www.itying.com  
http://www.ionic.wang/  
https://ionicframework.com/docs/api  
https://ionicons.com/  


## 环境准备
1. 安装nodejs
2. 安装cnpm 
npm install -g cnpm --registry=https://registry.npm.taobao.org
3. 安装Angular-cli 
npm install -g @angular/cli 或者 cnpm install -g @angular/cli

## 创建项目
ng new demo  
ng new --skip-install  
ng serve --open  

ng g component components/news  
ng g component components/home  
ng g component components/header  

ng g service services/storage.service  

ngAfterViewInit()//视图加载完成后触发的方法 建议把dom操作放在这个里面（原生js获取dom，或者@ViewChild()获取dom节点，且父组件可以通过@ViewChild()调用子组件的方法）

组件之间的方法一般不能直接调用

服务直接的方法可以相互调用

服务的方法可以被所有组件调用

Vscode里安装Angular 7 Snippets


父传子  @Input()  不但可以传递数据 而且可以传递方法  甚至可以传递整个父组件      
子传父  @ViewChild() 获取子组件,进而操作子组件的数据或方法  
		@Output() & EventEmitter  
		
非父子之间的通讯   localStorage 或 service

双向数据绑定 必须引入 FormsModule

带init的生命周期函数只会触发一次，带checked的每次数据或试图改变都会触发  父子传值时会触发ngOnChanges，ngDoChecked可以自定义一些检测操作，
卸载组件会触发ngOnDestroy
