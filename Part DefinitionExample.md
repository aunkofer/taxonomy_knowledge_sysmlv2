# A SysML v2 package containing 'part def' or 'Part Definition' example using textual sysml v2 notation

'''
package 'Part Definition Example' {
	import ScalarValues::*;
	
	part def Vehicle {
		attribute mass : Real;
		attribute status : VehicleStatus;
		
		part eng : Engine;
		
		ref part driver : Person;
	}
	
	attribute def VehicleStatus {
		attribute gearSetting : Integer;
		attribute acceleratorPosition : Real;
	}
	
	part def Engine;	
	part def Person;
}
'''