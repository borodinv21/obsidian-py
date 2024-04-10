Для того, чтобы установить `Bootstrap` воспользуемся следующей командой.
![[Pasted image 20240410174025.png]]
После этого вводим следующий код.
```JavaScript
import logo from './logo.svg';
import './App.css';
import { Button } from 'react-bootstrap';
import 'bootstrap/dist/css/bootstrap.min.css';

function App() {
	return (
		<>
			<h1>Hello, world</h1>
			<Button variant='primary'>Click</Button>
		</>
	);
}

export default App;
```
![[Pasted image 20240410174331.png]]
![[Pasted image 20240410174549.png]]