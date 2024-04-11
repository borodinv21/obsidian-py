[[useState]]

Для того, чтобы выводить текущее время, воспользуемся следующим кодом, где будем использовать хук `useState`.
![[Pasted image 20240411133344.png]]

```JavaScript
import logo from "/logo-name.svg";
import { useState } from "react";

export default function Header() {
	const [now, setNow] = useState(new Date());
	
	setInterval(() => {
		setNow(new Date());
	}, 1000);
	
	return (
		<header>
			<img src={logo} alt="" />
			<span>{now.toLocaleTimeString()}</span>
		</header>
	);
}
```
![[Pasted image 20240411133459.png]]