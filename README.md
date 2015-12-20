# JSON
##一、学习Json  

1、如何从后台获取Json对象，传到前台。  

    JSONArray jsonArray =JSONArray.fromObject(list);  

    response.getWriter().print(jsonArray.toString());  

      //其中： list里面放入的是Map对象，Map里面是 username和password键值对。  

      //前台可通过Ajax来解析Json。  

2、后台如何获取并解析前台的传来的Json对象  

    //拿到前台数据并转换为Json对象：  

    JSONArray jsonArray =JSONArray.fromObject(list);  

    for(int i = 0;i<jsonArray.length();i++){  

      JSONObject jsons = jsonArray.getJSONObject(i);  

      jsons.getInt("username");  

      jsons.getInt("password");  

    }
