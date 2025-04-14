# Sort-List-Map-Java-8


Sort List : 
==========

List<Employees> employees = Database.getEmployees();

employees.stream().sorted(Comparator.comparing(Employee::getName)).forEach(System.out::println);

employees.stream().sorted(Comparator.comparing(Employee::getDept)).forEach(System.out::println);

Sort Map :
=========

Map<String,Integer> map = new HashMap<>();
map.put("eight",8);
map.put("four",4);
map.put("ten",10);
map.put("two",2);

Now convert Map into List, How to do that.

List<Entry<String,Integer>> entries = new ArrayList<>(map.entrySet());

Ascending Order :
===============

employeeMap.entrySet().stream().sorted(Map.Entry.comparingByKey(Comparator.comparing(Employee::getSalary))).forEach(System.out::println);

Decending Order Based on Dept :
=============================

employeeMap.entrySet.stream().sorted(Map.Entry.comparingByKey(Comparator.comparing(Employee::getDept).reversed())).forEach(System.out::println);
