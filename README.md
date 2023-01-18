# caracter-mas-repetido
Ejercicio de JavaScript para encontrar el caracter más repetido en un string.


	const s = 'aLDFLAJDPjjeosne53o430';

	const solution = (s) => {
    	let mostCommon = [s[0]];
		let counter= [1];

		for (let i=1; i<s.length; i++) {
			if (!mostCommon.includes(s[i])){
				mostCommon.push(s[i])
				counter.push(1);
			} else {
				index= mostCommon.indexOf(s[i])
			}

			for (let a=0; a<i; a++){
				if (s[a]===s[i]) {
					counter[index]= counter[index]+1
				}
			}
		}

		indexOfMax= counter.indexOf(Math.max(...counter));
		return mostCommon[indexOfMax]
	}

	console.log(solution(s));
