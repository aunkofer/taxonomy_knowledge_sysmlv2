# A SysML v2 'Port Example' using textual sysml v2 notation

'''

package 'Port Example' {
	
	attribute def Temp;
	
	part def Fuel;
	
	port def FuelOutPort {
		attribute temperature : Temp;
		out item fuelSupply : Fuel;
		in item fuelReturn : Fuel;
	}
	
	port def FuelInPort {
		attribute temperature : Temp;
		in item fuelSupply : Fuel;
		out item fuelReturn : Fuel;
	}
	
	part def FuelTankAssembly {
		port fuelTankPort : FuelOutPort;
	}
	
	part def Engine {
		port engineFuelPort : FuelInPort;
	}
}

'''