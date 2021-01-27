# travel
// import 'package:2nd_project_dsc/2nd_project_dsc.dart' as 2nd_project_dsc;
import 'dart:io';

void main(List<String> arguments) {
  // ignore: omit_local_variable_types
  List tripList = [
    [1000, 'Alex', 200, 1 - 3 - 2021, 1000],
    [1001, 'Cairo', 200, 2 - 3 - 2021, 1200],
    [1002, 'Alex', 200, 3- 3 - 2021, 1000],
    [1003, 'Cairo', 200, 4 - 3 - 2021, 1200],
    [1004, 'Alex', 200, 5 - 3 - 2021, 1000],
    [1005, 'Cairo', 200, 6 - 3 - 2021, 1200],
    [1006, 'Alex', 200, 7 - 3 - 2021, 1000],
    [1007, 'Cairo', 200, 8 - 3 - 2021, 1200],
    [1008, 'Alex', 200, 9 - 3 - 2021, 1000],
    [1009, 'Cairo', 200, 10 - 3 - 2021, 1200],
    [1010, 'Alex', 200, 11 - 3 - 2021, 1000],
    [1011, 'Alex', 200, 12 - 3 - 2021, 1000],
    [1012, 'Cairo', 200, 13 - 3 - 2021, 1200],
    [1013, 'Alex', 200, 14 - 3 - 2021, 1000],
    [1014, 'Cairo', 200, 15 - 3 - 2021, 1200],
    [1015, 'Alex', 200, 16 - 3 - 2021, 1000],
    [1016, 'Alex', 200, 17 - 3 - 2021, 1000],
    [1017, 'Cairo', 200, 18 - 3 - 2021, 1200],
    [1018, 'Alex', 200, 19 - 3 - 2021, 1000],
    [1019, 'Cairo', 200, 20 - 3 - 2021, 1200],
    [1020, 'Alex', 200, 21 - 3 - 2021, 1000],
    [1021, 'Cairo', 200, 22 - 3 - 2021, 1200],
    [1022, 'Alex', 200, 23 - 3 - 2021, 1000],
    [1023, 'Cairo', 200, 24 - 3 - 2021, 1200],
    [1024, 'Alex', 200, 25 - 3 - 2021, 1000]
  ];

  Trip t = new Trip(2000, 'Mans', 200, DateTime.now(), 1203);
  t.addTrip(2000, 'Mans', 200, DateTime.now(), 1203);
  print('view trip = \n ${t.viewTrip([100, 'Mans', 200, DateTime.now(), 1203])}');
  print('----------------------------------------');
  print('the discount = ${t.discount(40000)}');
  print('----------------------------------------');
  print('the reversed trips = \n');
  t.reverseTrip(tripList);
  print('----------------------------------------');
  print('the deleted trips = \n ${t.deleteTrip(tripList)}');
  print('----------------------------------------');
  print('the latest 10 trips =');
  t.latestTenTrips(tripList);
  print('-----------------------------------------');
  // t.searchTrip(tripList, 1200);
  print(tripList[10][4].runtimeType);


  // t.searchTrip(tripList, 1200);
}

class Trip {
  //attributes
  int _id;
  String _location;
  final _passengerLimit = 200;
  DateTime _date;
  double _price;

  //constructor
  Trip(int id, String location, passengerLimit, DateTime date, double price) {
    this._id = id;
    this._location = location;
    passengerLimit = passengerLimit;
    this._date = date;
    this._price = price;
  }

  void set id(int id) {
    this._id = id;
  }

  int getid() {
    return _id;
  }

  void set location(String location) {
    this._location = _location;
  }

  String getlocation() {
    return _location;
  }

  void set date(DateTime date) {
    this._date = date;
  }

  DateTime getdate() {
    return _date;
  }

  void set price(double price) {
    this._price = price;
  }

  double getprice() {
    return _price;
  }
  
  
//addTrip method
  addTrip(
      int id, String location, passengerLimit, DateTime date, double price) {
    List addNewList = [];
    addNewList.addAll([10, 'mmm', 100, 2 - 2 - 2021, 1000.5]);
    // final DateFormat formatter = DateFormat('yyyy-MM-dd');
  }

//TODO
  editTrip(
      [int id, String location, passengerLimit, DateTime date, double price]) {
    List editedNewTrip = [];
  }

  //return a delete trip
  deleteTrip(List tripList) {
    return [] ;
  }

  //return the trip
  List viewTrip(List newList) {
    return newList;
  }

  //search for the price in the trips
  searchTrip(List tripList, double price) {
    //TODO for loop here is required
    for(int i = 0; i<tripList.length; i++){
      for(int j = 0; j<tripList[i].length; j++){
        if(tripList[i][j].contains(price))
        {
          print('is here');
        }
        else {
          print('non');
        }
      }
    }
  }

  //return the reversed trip              Done ==============
  reverseTrip(List tripList) {
    for (int i = tripList.length - 1; i >= 0; i--) {
      print(tripList[i]);
      // tripList.add(tripList[i][0]);
    }

  }

  //Bonus.. return the discount          Done ===============
  discount(double price) {
    if (price > 10000) {
      price -= (20 / 100) * price;
    }
    return price;
  }

  //return the latest 10
  List latestTenTrips(List tripList) {
    List newList = [];
    for (int i = tripList.length - 1; i > tripList.length - 12; i--) {
      print(tripList[i]);
    }
    // return(tripList);
  }
}
//

