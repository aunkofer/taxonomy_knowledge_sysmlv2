# A SysML v2 'Flow Connection Definition Example' using textual sysml v2 notation

'''

package 'Flow Connection Definition Example' {
	import 'Port Example'::*;
	
	part def Vehicle;
	
	flow def FuelFlow {
		ref :>> payload : Fuel;
		end port supplierPort : FuelOutPort;
		end port consumerPort : FuelInPort;
	}
	
	part vehicle : Vehicle {
		part tankAssy : FuelTankAssembly;
		part eng : Engine;
		
		flow : FuelFlow
		  from tankAssy.fuelTankPort.fuelSupply
			to eng.engineFuelPort.fuelSupply;
			
	} 
}

'''