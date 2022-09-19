# [[C]] condition
Conditions : 
		if (condition) { ... } else if (condition2) { ... } else { ... }
		Ternary Operator : 
			variable = (condition) ? expressionTrue : expressionFalse
			int time = 20; (time < 18) ? printf("Good day.") : printf("Good evening.");
		Switch : 
			Example : 
				switch (a) {
				  case 0:
				    break;  / break to avoid the "cascade" effect
				  case 1:
				    break;
				  default: // handle all the other cases
				    break;
				}

