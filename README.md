import 'package:flutter/material.dart';  

  

void main() => runApp(MyApp());  

  

class MyApp extends StatelessWidget {  

  // It is the root widget of your application.  

  @override  

  Widget build(BuildContext context) {  

    return MaterialApp(  

      title: 'Multiple Layout Widget',  

      debugShowCheckedModeBanner: false,  

      theme: ThemeData(  

        // This is the theme of your application.  

        primarySwatch: Colors.blue,  

      ),  

      home: MyHomePage(),  

    );  

  }  

}  

class MyHomePage extends StatelessWidget {  

  @override  

  Widget build(BuildContext context) {  

    return Center(  

      child: Container(  

        alignment: Alignment.center,  

        color: Colors.white,  

        child: Row(  

          children: <Widget>[  

            Expanded(  

              child: Text('Peter', textAlign: TextAlign.center),  

            ),  

            Expanded(  

              child: Text('John', textAlign: TextAlign.center ),  

  

            ),  

            Expanded(  

              child: FittedBox(  

                fit: BoxFit.contain, // otherwise the logo will be tiny  

                child: const FlutterLogo(),  

              ),  

            ),  

          ],  

        ),  

      ),  

    );  

  }  

}  
