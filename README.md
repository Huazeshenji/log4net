log4net 日志常见问题

1.如果在一个项目文件里面，在listview成功的打印日志，而且在相应的文件夹也生成了txt文件，说明配置是正确的。
（前提是日志项目正常）

2.如果引用日志类，也就是引用整个日志项目

1.如果要在新项目中单纯打印listview或者textbox（不生成txt文件），在该类前面先创建记录组件，接下来只要常规引用就行。



2.如果要在新项目文件夹中生成TXT日志文件，那么要做以下操作
1）需要在该项目下的AssemblyInfo.cs文件中添加下面的信息（没有就在项目属性，程序集信息自动生成，可以参考日志项目的同名文件）
[assembly: log4net.Config.XmlConfigurator(Watch = true)]
2）在新项目里面的相应的App.config也要加上相应的内容，内容和日志项目下log4net.config一模一样就行。
