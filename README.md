import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  final List<String> items = [
    'Groceries',
    'Workout',
    'Read a Book',
    'Call Mom',
    'Write Code',
    'Take a Walk',
    'Cook Dinner',
    'Watch a Movie',
    'Water Plants',
    'Plan Vacation',
    'Learn Flutter',
    'Play Guitar',
    'Meet Friends',
    'Go for a Run',
    'Clean House',
    'Practice Meditation',
    'Visit Library',
    'Listen to Music',
    'Shop for Clothes',
    'Write Journal',
  ];

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('GridView Example'),
        ),
        body: GridView.builder(
          gridDelegate: SliverGridDelegateWithFixedCrossAxisCount(
            crossAxisCount: 2,
          ),
          itemCount: items.length,
          itemBuilder: (context, index) {
            return Card(
              child: InkWell(
                onTap: () {
                  // Handle tap on item
                },
                child: Column(
                  mainAxisAlignment: MainAxisAlignment.center,
                  children: <Widget>[
                    Icon(Icons.check_circle),
                    SizedBox(height: 8),
                    Text(items[index]),
                  ],
                ),
              ),
            );
          },
        ),
      ),
    );
  }
}
