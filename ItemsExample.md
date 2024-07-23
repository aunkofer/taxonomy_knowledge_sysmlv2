# A SysML v2 'Items Example' using textual sysml v2 notation

'''

package 'Items Example' {
	import ScalarValues::*;
	
	item def Fuel;
	item def Person;
	
	part def Vehicle {
		attribute mass : Real;
		
		ref item driver : Person;

		part fuelTank {
			item fuel: Fuel;
		}		
	}
	
}

'''