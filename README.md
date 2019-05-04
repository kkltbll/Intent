# Intent
# 一、自定义WebView验证隐式Intent的使用
第一个应用：获取URL地址并启动隐式Intent的调用
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190504190055578.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNTg1ODAx,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019050419011322.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNTg1ODAx,size_16,color_FFFFFF,t_70)
关键代码：
 but1=(Button) findViewById(R.id.but1);
        text=(EditText)findViewById(R.id.text1) ;
        but1.setOnClickListener(new View.OnClickListener(){
            @Override
            public void onClick(View v) {
                Intent intent=new Intent();
                intent.setAction("android.intent.action.VIEW");
                String url=text.getText().toString();
                intent.putExtra("address",url);
                startActivity(intent);
            }
        });
