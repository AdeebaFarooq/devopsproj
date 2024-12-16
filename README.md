import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter App!!',
      debugShowCheckedModeBanner: false,
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Color(6463))
      ),
      home: Scaffold(appBar: AppBar(
        title: Text('hello world' ,style: Theme.of(context).textTheme.titleSmall,
),
             backgroundColor: Theme.of(context).colorScheme.primary,
              foregroundColor: Theme.of(context).colorScheme.primary,
      ),),
    );
  }
}


form program

import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo', // Title as String
      home: Scaffold(
        appBar: AppBar(title: const Text('Flutter Form')),
        body: const MyCustForm(),
      ),
    );
  }
}

class MyCustForm extends StatefulWidget {
  const MyCustForm({super.key});

  @override
  MyCustState createState() => MyCustState();
}

class MyCustState extends State<MyCustForm> {
  final _formKey = GlobalKey<FormState>();

  @override
  Widget build(BuildContext context) {
    return Form(
      key: _formKey,
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          TextFormField(
            decoration: const InputDecoration(
              labelText: 'Enter your name',
              icon: Icon(Icons.person),
            ),
          ),
          TextFormField(
            decoration: const InputDecoration(
              labelText: 'Enter your email',
              icon: Icon(Icons.email), // Corrected Icon widget
            ),
          ),
          Padding(
            padding: const EdgeInsets.symmetric(vertical: 16.0),
            child: ElevatedButton(
              child: const Text('Submit'),
              onPressed: null,
            ),
          ),
        ],
      ),
    );
  }
}
