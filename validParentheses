function validParentheses(parens) {
	if (parens === "") return true;
	else if (parens.length === 1) return false;
	else if (parens.length > 1 && parens[0] !== ")") {
		//reg;
		const reg = /[\r\n\t\f ]/; //if there is space or tab remove it first;
		parens = [...parens].filter((paren) => !reg.test(paren));
		const addParen = [];
		parens.forEach((current, index) => {
			if (!addParen.length) addParen.push(current);
			else {
				if (current === addParen[addParen.length - 1]) addParen.push(current);
				else if (addParen[addParen.length - 1].charCodeAt(0) === "(".charCodeAt()) {
					addParen.pop();
				}
			}
		});
		return addParen.length ? false : true;
	} else return false;
}

/*
"(()())"              =>  true
"()()))"            =>  false
"("                 =>  false
"(())((()())())"    =>  true

"())("
 */
const valid = validParentheses("())(");
console.log(valid);
