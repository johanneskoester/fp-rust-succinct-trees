# Phase 1: Rust

Zu Beginn des Fachprojekts werden die Grundlagen von Rust anhand von praktischen Übungen gelernt.  
Zunächst muss der Poolrechner für die folgenden Übungen eingerichtet werden. Dazu installieren Sie bitte den Paketmanager Conda, wie [hier](https://conda.io/docs/user-guide/install/linux.html#installing-on-linux) beschrieben. Wählen Sie die Variante **Miniconda** und beantworten Sie alle Fragen mit **yes**. Danach installieren Sie bitte **Rust** \(Der Rust-Compiler und relevante Tools\) und **Exercism** \(Ein Kommandozeilen-Tool zum Download von Übungen\):

```
conda install -c conda-forge rust exercism
```

## Einführung

Lesen Sie [Abschnitt 1.2 im Rust-Buch](https://doc.rust-lang.org/book/second-edition/ch01-02-hello-world.html) und führen die dort beschriebenen Schritte aus.   
Anschließend lesen Sie [Abschnitt 2 im Rust-Buch](https://doc.rust-lang.org/book/second-edition/ch02-00-guessing-game-tutorial.html) und führen die dort beschriebenen Schritte aus.

## Vertiefung

Im folgenden werden alle relevanten Aspekte von Rust erarbeitet, in dem jeweils ein Kapitel im Rust-Buch gelesen wird und ergänzende Übungen durchgeführt werden. Die Übungen kommen von [Rustlings](https://github.com/carols10cents/rustlings) und [Exercism](http://exercism.io/languages/rust/exercises). Im Falle von Rustlings kann die Übung direkt im Browser ausgeführt werden. Exercism-Übungen werden über das oben installierte Kommandozeilentool heruntergeladen. Zusätzlich ist es sinnvoll die Buch-Kapitel nicht nur zu lesen sondern die Beispiele selbst nachzuvollziehen.

| Sprachaspekt | Lesen | Üben |
| --- | --- | --- |
| Variablen | [3.1](https://doc.rust-lang.org/book/second-edition/ch03-01-variables-and-mutability.html) | [1](https://play.rust-lang.org/?code=%2F%2F+variables1.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++x+%3D+5%3B
++++println!%28"x+has+the+value+{}"%2C+x%29%3B
}

































%2F%2F+Hint%3A+The+declaration+on+line+5+is+missing+a+keyword+that+is+needed+in+Rust
%2F%2F+to+create+a+new+variable+binding.
),  [2](https://play.rust-lang.org/?code=%2F%2F+variables2.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++let+x%3B
++++if+x+%3D%3D+10+{
++++++++println!%28"Ten!"%29%3B
++++}+else+{
++++++++println!%28"Not+ten!"%29%3B
++++}
}





























%2F%2F+The+compiler+message+is+saying+that+Rust+cannot+infer+the+type+that+the
%2F%2F+variable+binding+`x`+has+with+what+is+given+here.
%2F%2F+What+happens+if+you+annotate+line+5+with+a+type+annotation%3F
%2F%2F+What+if+you+give+x+a+value%3F
%2F%2F+What+if+you+do+both%3F
%2F%2F+What+type+should+x+be%2C+anyway%3F
%2F%2F+What+if+x+is+the+same+type+as+10%3F+What+if+it's+a+different+type%3F
), [3](https://play.rust-lang.org/?code=%2F%2F+variables3.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++let+x+%3D+3%3B
++++println!%28"Number+{}"%2C+x%29%3B
++++x+%3D+5%3B
++++println!%28"Number+{}"%2C+x%29%3B
}































%2F%2F+In+Rust%2C+variable+bindings+are+immutable+by+default.+But+here+we're+trying
%2F%2F+to+reassign+a+different+value+to+x!+There's+a+keyword+we+can+use+to+make
%2F%2F+a+variable+binding+mutable+instead.
), [4](https://play.rust-lang.org/?code=%2F%2F+variables4.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++let+x%3A+i32%3B
++++println!%28"Number+{}"%2C+x%29%3B
}

































%2F%2F+Oops!+In+this+exercise%2C+we+have+a+variable+binding+that+we've+created+on
%2F%2F+line+5%2C+and+we're+trying+to+use+it+on+line+6%2C+but+we+haven't+given+it+a
%2F%2F+value.+We+can't+print+out+something+that+isn't+there%3B+try+giving+x+a+value!
%2F%2F+This+is+an+error+that+can+cause+bugs+that's+very+easy+to+make+in+any
%2F%2F+programming+language+--+thankfully+the+Rust+compiler+has+caught+this+for+us!
) |
| Datentypen | [3.2](https://doc.rust-lang.org/book/second-edition/ch03-02-data-types.html), [arrays](https://doc.rust-lang.org/std/primitive.array.html) | [1](https://play.rust-lang.org/?code=%2F%2F+primitive_types1.rs
%2F%2F+Fill+in+the+rest+of+the+line+that+has+code+missing!
%2F%2F+No+hints%2C+there's+no+tricks%2C+just+get+used+to+typing+these+%3A%29

fn+main%28%29+{
++++%2F%2F+Booleans+%28`bool`%29

++++let+is_morning+%3D+true%3B
++++if+is_morning+{
++++++++println!%28"Good+morning!"%29%3B
++++}

++++let+%2F%2F+Finish+the+rest+of+this+line+like+the+example!+Or+make+it+be+false!
++++if+is_evening+{
++++++++println!%28"Good+evening!"%29%3B
++++}
}
), [2](https://play.rust-lang.org/?code=%2F%2F+primitive_types2.rs
%2F%2F+Fill+in+the+rest+of+the+line+that+has+code+missing!
%2F%2F+No+hints%2C+there's+no+tricks%2C+just+get+used+to+typing+these+%3A%29

fn+main%28%29+{
++++%2F%2F+Characters+%28`char`%29

++++let+my_first_initial+%3D+'C'%3B
++++if+my_first_initial.is_alphabetic%28%29+{
++++++++println!%28"Alphabetical!"%29%3B
++++}+else+if+my_first_initial.is_numeric%28%29+{
++++++++println!%28"Numerical!"%29%3B
++++}+else+{
++++++++println!%28"Neither+alphabetic+nor+numeric!"%29%3B
++++}

++++let+%2F%2F+Finish+this+line+like+the+example!+What's+your+favorite+character%3F
++++%2F%2F+Try+a+letter%2C+try+a+number%2C+try+a+special+character%2C+try+a+character
++++%2F%2F+from+a+different+language+than+your+own%2C+try+an+emoji!
++++if+your_character.is_alphabetic%28%29+{
++++++++println!%28"Alphabetical!"%29%3B
++++}+else+if+your_character.is_numeric%28%29+{
++++++++println!%28"Numerical!"%29%3B
++++}+else+{
++++++++println!%28"Neither+alphabetic+nor+numeric!"%29%3B
++++}
}
), [3](https://play.rust-lang.org/?code=%2F%2F+primitive_types3.rs
%2F%2F+Create+an+array+with+at+least+100+elements+in+it+where+the+%3F%3F%3F+is.+
%2F%2F+Scroll+down+for+hints!

fn+main%28%29+{
++++let+a+%3D+%3F%3F%3F

++++if+a.len%28%29+>%3D+100+{
++++++++println!%28"Wow%2C+that's+a+big+array!"%29%3B
++++}+else+{
++++++++println!%28"Meh%2C+I+eat+arrays+like+that+for+breakfast."%29%3B
++++}
}



























%2F%2F+There's+a+shorthand+to+initialize+Arrays+with+a+certain+size+that+does+not+
%2F%2F+require+you+to+type+in+100+items+%28but+you+certainly+can+if+you+want!%29
%2F%2F+Check+out+the+Primitive+Types+->+Arrays+section+of+the+book%3A
%2F%2F+https%3A%2F%2Fdoc.rust-lang.org%2Fstable%2Fbook%2Fsecond-edition%2Fch03-02-data-types.html%23arrays
%2F%2F+Bonus%3A+what+are+some+other+things+you+could+have+that+would+return+true
%2F%2F+for+`a.len%28%29+>%3D+100`%3F
), [4](https://play.rust-lang.org/?code=%2F%2F+primitive_types5.rs
%2F%2F+Destructure+the+`cat`+tuple+so+that+the+println+will+work.
%2F%2F+Scroll+down+for+hints!

fn+main%28%29+{
++++let+cat+%3D+%28"Furry+McFurson"%2C+3.5%29%3B
++++let+%2F*+your+pattern+here+*%2F+%3D+cat%3B

++++println!%28"{}+is+{}+years+old."%2C+name%2C+age%29%3B
}






























%2F%2F+Take+a+look+at+the+Primitive+Types+->+Tuples+section+of+the+book%3A
%2F%2F+http%3A%2F%2Fdoc.rust-lang.org%2Fstable%2Fbook%2Fprimitive-types.html%23tuples
%2F%2F+Particularly+the+part+about+"destructuring+lets".+You'll+need+to
%2F%2F+make+a+pattern+to+bind+`name`+and+`age`+to+the+appropriate+parts
%2F%2F+of+the+tuple.+You+can+do+it!!
), [5](https://play.rust-lang.org/?code=%2F%2F+primitive_types6.rs
%2F%2F+Use+a+tuple+index+to+access+the+second+element+of+`numbers`.
%2F%2F+You+can+put+this+right+into+the+`println!`+where+the+%3F%3F%3F+is.
%2F%2F+Scroll+down+for+hints!

fn+main%28%29+{
++++let+numbers+%3D+%281%2C+2%2C+3%29%3B
++++println!%28"The+second+number+is+{}"%2C+%3F%3F%3F%29%3B
}































%2F%2F+While+you+could+use+a+destructuring+`let`+for+the+tuple+here%2C+try+
%2F%2F+indexing+into+it+instead%2C+as+explained+here%3A
%2F%2F+http%3A%2F%2Fdoc.rust-lang.org%2Fstable%2Fbook%2Fprimitive-types.html%23tuple-indexing
%2F%2F+Now+you+have+another+tool+in+your+toolbox!
) |
| Funktionen | [3.3](https://doc.rust-lang.org/book/second-edition/ch03-03-how-functions-work.html) | [1](https://play.rust-lang.org/?code=%2F%2F+functions1.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++call_me%28%29%3B
}


































%2F%2F+This+main+function+is+calling+a+function+that+it+expects+to+exist%2C+but+the
%2F%2F+function+doesn't+exist.+It+expects+this+function+to+have+the+name+`call_me`.
%2F%2F+It+expects+this+function+to+not+take+any+arguments+and+not+return+a+value.
%2F%2F+Sounds+a+lot+like+`main`%2C+doesn't+it%3F
), [2](https://play.rust-lang.org/?code=%2F%2F+functions2.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++call_me%283%29%3B
}

fn+call_me%28num%29+{
++++for+i+in+0..num+{
++++++++println!%28"Ring!+Call+number+{}"%2C+i+%2B+1%29%3B
++++}
}




























%2F%2F+Rust+requires+that+all+parts+of+a+function's+signature+have+type+annotations%2C
%2F%2F+but+`call_me`+is+missing+the+type+annotation+of+`num`.
), [3](https://play.rust-lang.org/?code=%2F%2F+functions3.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++call_me%28%29%3B
}

fn+call_me%28num%3A+i32%29+{
++++for+i+in+0..num+{
++++++++println!%28"Ring!+Call+number+{}"%2C+i+%2B+1%29%3B
++++}
}




























%2F%2F+This+time%2C+the+function+*declaration*+is+okay%2C+but+there's+something+wrong
%2F%2F+with+the+place+where+we're+calling+the+function.
), [4](https://play.rust-lang.org/?code=%2F%2F+functions4.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

%2F%2F+This+store+is+having+a+sale+where+if+the+price+is+an+even+number%2C+you+get
%2F%2F+10+%28money+unit%29+off%2C+but+if+it's+an+odd+number%2C+it's+3+%28money+unit%29+less.

fn+main%28%29+{
++++let+original_price+%3D+51%3B
++++println!%28"Your+sale+price+is+{}"%2C+sale_price%28original_price%29%29%3B
}

fn+sale_price%28price%3A+i32%29+->+{
++++if+is_even%28price%29+{
++++++++price+-+10
++++}+else+{
++++++++price+-+3
++++}
}

fn+is_even%28num%3A+i32%29+->+bool+{
++++num+%+2+%3D%3D+0
}



















%2F%2F+The+error+message+points+to+line+12+and+says+it+expects+a+type+after+the
%2F%2F+`->`.+This+is+where+the+function's+return+type+should+be--+take+a+look+at
%2F%2F+the+`is_even`+function+for+an+example!
), [5](https://play.rust-lang.org/?code=%2F%2F+functions5.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++let+answer+%3D+square%283%29%3B
++++println!%28"The+answer+is+{}"%2C+answer%29%3B
}

fn+square%28num%3A+i32%29+->+i32+{
++++num+*+num%3B
}





























%2F%2F+This+is+a+really+common+error+that+can+be+fixed+by+removing+one+character.
%2F%2F+It+happens+because+Rust+distinguishes+between+expressions+and+statements%3A+expressions+return
%2F%2F+a+value+and+statements+don't.+We+want+to+return+a+value+from+the+`square`+function%2C+but+it
%2F%2F+isn't+returning+one+right+now...
) |
| Kontrolfluss | [3.5](https://doc.rust-lang.org/book/second-edition/ch03-05-control-flow.html) | [1](https://play.rust-lang.org/?code=%2F%2F+if1.rs

pub+fn+bigger%28a%3A+i32%2C+b%3Ai32%29+->+i32+{
++++%2F%2F+Complete+this+function+to+return+the+bigger+number!
++++%2F%2F+Do+not+use%3A
++++%2F%2F+-+return
++++%2F%2F+-+another+function+call
++++%2F%2F+-+additional+variables
++++%2F%2F+Scroll+down+for+hints.
}

%23[cfg%28test%29]
mod+tests+{
++++use+super%3A%3A*%3B

++++%23[test]
++++fn+ten_is_bigger_than_eight%28%29+{
++++++++assert_eq!%2810%2C+bigger%2810%2C+8%29%29%3B
++++}

++++%23[test]
++++fn+fortytwo_is_bigger_than_thirtytwo%28%29+{
++++++++assert_eq!%2842%2C+bigger%2832%2C+42%29%29%3B
++++}
}

























%2F%2F+It's+possible+to+do+this+in+one+line+if+you+would+like!
%2F%2F+Some+similar+examples+from+other+languages%3A
%2F%2F+-+In+C%28%2B%2B%29+this+would+be%3A+`a+>+b+%3F+a+%3A+b`
%2F%2F+-+In+Python+this+would+be%3A++`a+if+a+>+b+else+b`
%2F%2F+Remember+in+Rust+that%3A
%2F%2F+-+the+`if`+condition+does+not+need+to+be+surrounded+by+parentheses
%2F%2F+-+`if`%2F`else`+conditionals+are+expressions
%2F%2F+-+Each+condition+is+followed+by+a+`{}`+block.
), [2](http://exercism.io/exercises/rust/leap/readme) |
| Ownership | [4](https://doc.rust-lang.org/book/second-edition/ch04-00-understanding-ownership.html) | [1](https://play.rust-lang.org/?code=%2F%2F+move_semantics1.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

pub+fn+main%28%29+{
++++let+vec0+%3D+Vec%3A%3Anew%28%29%3B

++++let+vec1+%3D+fill_vec%28vec0%29%3B

++++println!%28"{}+has+length+{}+content+`{%3A%3F}`"%2C+"vec1"%2C+vec1.len%28%29%2C+vec1%29%3B

++++vec1.push%2888%29%3B

++++println!%28"{}+has+length+{}+content+`{%3A%3F}`"%2C+"vec1"%2C+vec1.len%28%29%2C+vec1%29%3B

}

fn+fill_vec%28vec%3A+Vec<i32>%29+->+Vec<i32>+{
++++let+mut+vec+%3D+vec%3B

++++vec.push%2822%29%3B
++++vec.push%2844%29%3B
++++vec.push%2866%29%3B

++++vec
}















%2F%2F+So+you've+got+the+"cannot+borrow+immutable+local+variable+`vec1`+as+mutable"+error+on+line+11%2C
%2F%2F+right%3F+The+fix+for+this+is+going+to+be+adding+one+keyword%2C+and+the+addition+is+NOT+on+line+11
%2F%2F+where+the+error+is.
), [2](https://play.rust-lang.org/?code=%2F%2F+move_semantics2.rs
%2F%2F+Make+me+compile+without+changing+line+10!+Scroll+down+for+hints+%3A%29

pub+fn+main%28%29+{
++++let+vec0+%3D+Vec%3A%3Anew%28%29%3B

++++let+mut+vec1+%3D+fill_vec%28vec0%29%3B

++++%2F%2F+Do+not+change+the+following+line!
++++println!%28"{}+has+length+{}+content+`{%3A%3F}`"%2C+"vec0"%2C+vec0.len%28%29%2C+vec0%29%3B

++++vec1.push%2888%29%3B

++++println!%28"{}+has+length+{}+content+`{%3A%3F}`"%2C+"vec1"%2C+vec1.len%28%29%2C+vec1%29%3B

}

fn+fill_vec%28vec%3A+Vec<i32>%29+->+Vec<i32>+{
++++let+mut+vec+%3D+vec%3B

++++vec.push%2822%29%3B
++++vec.push%2844%29%3B
++++vec.push%2866%29%3B

++++vec
}














%2F%2F+So+`vec0`+is+being+*moved*+into+the+function+`fill_vec`+when+we+call+it+on
%2F%2F+line+7%2C+which+means+it+gets+dropped+at+the+end+of+`fill_vec`%2C+which+means+we
%2F%2F+can't+use+`vec0`+again+on+line+10+%28or+anywhere+else+in+`main`+after+the
%2F%2F+`fill_vec`+call+for+that+matter%29.+We+could+fix+this+in+a+few+ways%2C+try+them
%2F%2F+all!
%2F%2F+1.+Make+another%2C+separate+version+of+the+data+that's+in+`vec0`+and+pass+that
%2F%2F+to+`fill_vec`+instead.
%2F%2F+2.+Make+`fill_vec`+borrow+its+argument+instead+of+taking+ownership+of+it%2C
%2F%2F+and+then+copy+the+data+within+the+function+in+order+to+return+an+owned
%2F%2F+`Vec<i32>`
%2F%2F+3.+Make+`fill_vec`+*mutably*+borrow+its+argument+%28which+will+need+to+be
%2F%2F+mutable%29%2C+modify+it+directly%2C+then+not+return+anything.+Then+you+can+get+rid
%2F%2F+of+`vec1`+entirely+--+note+that+this+will+change+what+gets+printed+by+the
%2F%2F+first+`println!`
), [3](https://play.rust-lang.org/?code=%2F%2F+move_semantics3.rs
%2F%2F+Make+me+compile+without+adding+new+lines--+just+changing+existing+lines!
%2F%2F+%28no+lines+with+multiple+semicolons+necessary!%29
%2F%2F+Scroll+down+for+hints+%3A%29

pub+fn+main%28%29+{
++++let+vec0+%3D+Vec%3A%3Anew%28%29%3B

++++let+mut+vec1+%3D+fill_vec%28vec0%29%3B

++++println!%28"{}+has+length+{}+content+`{%3A%3F}`"%2C+"vec1"%2C+vec1.len%28%29%2C+vec1%29%3B

++++vec1.push%2888%29%3B

++++println!%28"{}+has+length+{}+content+`{%3A%3F}`"%2C+"vec1"%2C+vec1.len%28%29%2C+vec1%29%3B

}

fn+fill_vec%28vec%3A+Vec<i32>%29+->+Vec<i32>+{
++++vec.push%2822%29%3B
++++vec.push%2844%29%3B
++++vec.push%2866%29%3B

++++vec
}

















%2F%2F+The+difference+between+this+one+and+the+previous+ones+is+that+the+first+line
%2F%2F+of+`fn+fill_vec`+that+had+`let+mut+vec+%3D+vec%3B`+is+no+longer+there.+You+can%2C
%2F%2F+instead+of+adding+that+line+back%2C+add+`mut`+in+one+place+that+will+change
%2F%2F+an+existing+binding+to+be+a+mutable+binding+instead+of+an+immutable+one+%3A%29
), [4](https://play.rust-lang.org/?code=%2F%2F+move_semantics4.rs
%2F%2F+Refactor+this+code+so+that+instead+of+having+`vec0`+and+creating+the+vector
%2F%2F+in+`fn+main`%2C+we+instead+create+it+within+`fn+fill_vec`+and+transfer+the
%2F%2F+freshly+created+vector+from+fill_vec+to+its+caller.+Scroll+for+hints!

pub+fn+main%28%29+{
++++let+vec0+%3D+Vec%3A%3Anew%28%29%3B

++++let+mut+vec1+%3D+fill_vec%28vec0%29%3B

++++println!%28"{}+has+length+{}+content+`{%3A%3F}`"%2C+"vec1"%2C+vec1.len%28%29%2C+vec1%29%3B

++++vec1.push%2888%29%3B

++++println!%28"{}+has+length+{}+content+`{%3A%3F}`"%2C+"vec1"%2C+vec1.len%28%29%2C+vec1%29%3B

}

fn+fill_vec%28vec%3A+Vec<i32>%29+->+Vec<i32>+{
++++let+mut+vec+%3D+vec%3B

++++vec.push%2822%29%3B
++++vec.push%2844%29%3B
++++vec.push%2866%29%3B

++++vec
}












%2F%2F+Stop+reading+whenever+you+feel+like+you+have+enough+direction+%3A%29+Or+try
%2F%2F+doing+one+step+and+then+fixing+the+compiler+errors+that+result!
%2F%2F+So+the+end+goal+is+to%3A
%2F%2F+-+get+rid+of+the+first+line+in+main+that+creates+the+new+vector
%2F%2F+-+so+then+`vec0`+doesn't+exist%2C+so+we+can't+pass+it+to+`fill_vec`
%2F%2F+-+we+don't+want+to+pass+anything+to+`fill_vec`%2C+so+its+signature+should
%2F%2F+++reflect+that+it+does+not+take+any+arguments
%2F%2F+-+since+we're+not+creating+a+new+vec+in+`main`+anymore%2C+we+need+to+create
%2F%2F+++a+new+vec+in+`fill_vec`%2C+similarly+to+the+way+we+did+in+`main`
), [5](https://play.rust-lang.org/?code=%2F%2F+primitive_types4.rs
%2F%2F+Get+a+slice+out+of+Array+a+where+the+%3F%3F%3F+is+so+that+the+`if`+statement
%2F%2F+returns+true.+Scroll+down+for+hints!!

fn+main%28%29+{
++++let+a+%3D+[1%2C+2%2C+3%2C+4%2C+5]%3B

++++let+nice_slice+%3D+%3F%3F%3F

++++if+nice_slice+%3D%3D+[2%2C+3%2C+4]+{
++++++++println!%28"Nice+slice!"%29%3B
++++}+else+{
++++++++println!%28"Not+quite+what+I+was+expecting...+I+see%3A+{%3A%3F}"%2C+nice_slice%29%3B
++++}
}

























%2F%2F+Take+a+look+at+the+Primitive+Types+->+Slices+section+of+the+book%3A
%2F%2F+http%3A%2F%2Fdoc.rust-lang.org%2Fstable%2Fbook%2Fprimitive-types.html%23slices
%2F%2F+and+use+the+starting+and+ending+indices+of+the+items+in+the+Array
%2F%2F+that+you+want+to+end+up+in+the+slice.

%2F%2F+If+you're+curious+why+the+right+hand+of+the+`%3D%3D`+comparison+does+not
%2F%2F+have+an+ampersand+for+a+reference+since+the+left+hand+side+is+a
%2F%2F+reference%2C+take+a+look+at+the+Deref+coercions+chapter%3A
%2F%2F+http%3A%2F%2Fdoc.rust-lang.org%2Fstable%2Fbook%2Fderef-coercions.html
) |
| Structs | [5](https://doc.rust-lang.org/book/second-edition/ch05-00-structs.html) | [1](http://exercism.io/exercises/rust/clock/readme) |
| Strings | [8.1](https://doc.rust-lang.org/book/second-edition/ch08-02-strings.html) | [1](https://play.rust-lang.org/?code=%2F%2F+strings1.rs
%2F%2F+Make+me+compile+without+changing+the+function+signature!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++let+answer+%3D+current_favorite_color%28%29%3B
++++println!%28"My+current+favorite+color+is+{}"%2C+answer%29%3B
}

fn+current_favorite_color%28%29+->+String+{
++++"blue"
}





























%2F%2F+The+`current_favorite_color`+function+is+currently+returning+a+string+slice+with+the+`'static`
%2F%2F+lifetime.+We+know+this+because+the+data+of+the+string+lives+in+our+code+itself+--+it+doesn't
%2F%2F+come+from+a+file+or+user+input+or+another+program+--+so+it+will+live+as+long+as+our+program
%2F%2F+lives.+But+it+is+still+a+string+slice.+There's+one+way+to+create+a+`String`+by+converting+a
%2F%2F+string+slice+covered+in+the+Strings+chapter+of+the+book%2C+and+another+way+that+uses+the+`From`
%2F%2F+trait.
), [2](https://play.rust-lang.org/?code=%2F%2F+strings2.rs
%2F%2F+Make+me+compile+without+changing+the+function+signature!+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++let+word+%3D+String%3A%3Afrom%28"green"%29%3B+%2F%2F+Try+not+changing+this+line+%3A%29
++++if+is_a_color_word%28word%29+{
++++++++println!%28"That+is+a+color+word+I+know!"%29%3B
++++}+else+{
++++++++println!%28"That+is+not+a+color+word+I+know."%29%3B
++++}
}

fn+is_a_color_word%28attempt%3A+%26str%29+->+bool+{
++++attempt+%3D%3D+"green"+||+attempt+%3D%3D+"blue"+||+attempt+%3D%3D+"red"
}


























%2F%2F+Yes%2C+it+would+be+really+easy+to+fix+this+by+just+changing+the+value+bound+to+`word`+to+be+a
%2F%2F+string+slice+instead+of+a+`String`%2C+wouldn't+it%3F%3F+There+is+a+way+to+add+one+character+to+line
%2F%2F+6%2C+though%2C+that+will+coerce+the+`String`+into+a+string+slice.
), [3](https://play.rust-lang.org/?code=%2F%2F+strings3.rs
%2F%2F+Ok%2C+here+are+a+bunch+of+values--+some+are+`Strings`%2C+some+are+`%26strs`.+Your
%2F%2F+task+is+to+call+one+of+these+two+functions+on+each+value+depending+on+what
%2F%2F+you+think+each+value+is.+That+is%2C+add+either+`string_slice`+or+`string`
%2F%2F+before+the+parentheses+on+each+line.+If+you're+right%2C+it+will+compile!

fn+string_slice%28arg%3A+%26str%29+{+println!%28"{}"%2C+arg%29%3B+}
fn+string%28arg%3A+String%29+{+println!%28"{}"%2C+arg%29%3B+}

fn+main%28%29+{
++++%28"blue"%29%3B
++++%28"red".to_string%28%29%29%3B
++++%28String%3A%3Afrom%28"hi"%29%29%3B
++++%28"rust+is+fun!".to_owned%28%29%29%3B
++++%28"nice+weather".into%28%29%29%3B
++++%28format!%28"Interpolation+{}"%2C+"Station"%29%29%3B
++++%28%26String%3A%3Afrom%28"abc"%29[0..1]%29%3B
++++%28"++hello+there+".trim%28%29%29%3B
++++%28"Happy+Monday!".to_string%28%29.replace%28"Mon"%2C+"Tues"%29%29%3B
++++%28"mY+sHiFt+KeY+iS+sTiCkY".to_lowercase%28%29%29%3B
}
) |
| Enumerations and pattern matching | [6.1](https://doc.rust-lang.org/book/second-edition/ch06-01-defining-an-enum.html) | [1](https://play.rust-lang.org/?code=enum+WebEvent+{
++++PageLoad%2C
++++PageUnload%2C
++++KeyPress%28char%29%2C
++++Paste%28String%29%2C
++++Click+{+x%3A+i64%2C+y%3A+i64+}%2C
}


fn+inspect%28event%3A+WebEvent%29+{
++++match+event+{
++++++++WebEvent%3A%3AKeyPress%28c%29+%3D>+println!%28"pressed+'{}'."%2C+c%29%2C
++++++++%2F%2F+implement+all+other+variant+of+the+enum+with+appropriate+output
++++}
}


fn+main%28%29+{
++++inspect%28WebEvent%3A%3APageLoad%29%3B
++++inspect%28WebEvent%3A%3APageUnload%29%3B
++++inspect%28WebEvent%3A%3AKeyPress%28'a'%29%29%3B
++++inspect%28WebEvent%3A%3APaste%28"ABC".to_owned%28%29%29%29%3B
++++inspect%28WebEvent%3A%3AClick+{x%3A+1%2C+y%3A+2}%29%3B
}
) |
| Modules | [7](https://doc.rust-lang.org/book/second-edition/ch07-00-modules.html) | [1](https://play.rust-lang.org/?code=%2F%2F+modules1.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

mod+sausage_factory+{
++++fn+make_sausage%28%29+{
++++++++println!%28"sausage!"%29%3B
++++}
}

fn+main%28%29+{
++++sausage_factory%3A%3Amake_sausage%28%29%3B
}




























%2F%2F+Everything+is+private+in+Rust+by+default--+but+there's+a+keyword+we+can+use
%2F%2F+to+make+something+public!+The+compiler+error+should+point+to+the+thing+that
%2F%2F+needs+to+be+public.
), [2](https://play.rust-lang.org/?code=%2F%2F+modules2.rs
%2F%2F+Make+me+compile!+Scroll+down+for+hints+%3A%29

mod+us_presidential_frontrunners+{
++++use+self%3A%3Ademocrats%3A%3AHILLARY_CLINTON+as+democrat%3B
++++use+self%3A%3Arepublicans%3A%3ADONALD_TRUMP+as+republican%3B

++++mod+democrats+{
++++++++pub+const+HILLARY_CLINTON%3A+%26'static+str+%3D+"Hillary+Clinton"%3B
++++++++pub+const+BERNIE_SANDERS%3A+%26'static+str+%3D+"Bernie+Sanders"%3B
++++}

++++mod+republicans+{
++++++++pub+const+DONALD_TRUMP%3A+%26'static+str+%3D+"Donald+Trump"%3B
++++++++pub+const+JEB_BUSH%3A+%26'static+str+%3D+"Jeb+Bush"%3B
++++}
}

fn+main%28%29+{
++++println!%28"candidates%3A+{}+and+{}"%2C
+++++++++++++us_presidential_frontrunners%3A%3Ademocrat%2C
+++++++++++++us_presidential_frontrunners%3A%3Arepublican%29%3B
}

















%2F%2F+The+us_presidential_frontrunners+module+is+trying+to+present+an+external
%2F%2F+interface+%28the+`democrat`+and+`republican`+constants%29+that+is+different+than
%2F%2F+its+internal+structure+%28the+`democrats`+and+`republicans`+modules+and
%2F%2F+associated+constants%29.+It's+almost+there+except+for+one+keyword+missing+for
%2F%2F+each+constant.
) |
| Tests | [11](https://doc.rust-lang.org/book/second-edition/ch11-00-testing.html) | [1](https://play.rust-lang.org/?code=%2F%2F+tests1.rs
%2F%2F+Tests+are+important+to+ensure+that+your+code+does+what+you+think+it+should+do.
%2F%2F+Tests+can+be+run+on+this+file+with+the+following+command%3A
%2F%2F+rustc+--test+tests1.rs

%2F%2F+This+test+has+a+problem+with+it+--+make+the+test+compile!+Make+the+test
%2F%2F+pass!+Make+the+test+fail!+Scroll+down+for+hints+%3A%29

%23[cfg%28test%29]
mod+tests+{
++++%23[test]
++++fn+you_can_assert%28%29+{
++++++++assert!%28%29%3B
++++}
}





























%2F%2F+You+don't+even+need+to+write+any+code+to+test+--+you+can+just+test+values+and+run+that%2C+even
%2F%2F+though+you+wouldn't+do+that+in+real+life+%3A%29+`assert!`+is+a+macro+that+needs+an+argument.
%2F%2F+Depending+on+the+value+of+the+argument%2C+`assert!`+will+do+nothing+%28in+which+case+the+test+will
%2F%2F+pass%29+or+`assert!`+will+panic+%28in+which+case+the+test+will+fail%29.+So+try+giving+different+values
%2F%2F+to+`assert!`+and+see+which+ones+compile%2C+which+ones+pass%2C+and+which+ones+fail+%3A%29
), [2](https://play.rust-lang.org/?code=%2F%2F+tests2.rs
%2F%2F+This+test+has+a+problem+with+it+--+make+the+test+compile!+Make+the+test
%2F%2F+pass!+Make+the+test+fail!+Scroll+down+for+hints+%3A%29

%23[cfg%28test%29]
mod+tests+{
++++%23[test]
++++fn+you_can_assert_eq%28%29+{
++++++++assert_eq!%28%29%3B
++++}
}





























%2F%2F+Like+the+previous+exercise%2C+you+don't+need+to+write+any+code+to+get+this+test+to+compile+and
%2F%2F+run.+`assert_eq!`+is+a+macro+that+takes+two+arguments+and+compares+them.+Try+giving+it+two
%2F%2F+values+that+are+equal!+Try+giving+it+two+arguments+that+are+different!+Try+giving+it+two+values
%2F%2F+that+are+of+different+types!+Try+switching+which+argument+comes+first+and+which+comes+second!
), [3](https://play.rust-lang.org/?code=%2F%2F+tests3.rs
%2F%2F+This+test+isn't+testing+our+function+--+make+it+do+that+in+such+a+way+that
%2F%2F+the+test+passes.+Then+write+a+second+test+that+tests+that+we+get+the+result
%2F%2F+we+expect+to+get+when+we+call+`is_even%285%29`.+Scroll+down+for+hints!

pub+fn+is_even%28num%3A+i32%29+->+bool+{
++++num+%+2+%3D%3D+0
}

%23[cfg%28test%29]
mod+tests+{
++++use+super%3A%3A*%3B

++++%23[test]
++++fn+is_true_when_even%28%29+{
++++++++assert!%28false%29%3B
++++}
}






















%2F%2F+You+can+call+a+function+right+where+you're+passing+arguments+to+`assert!`+--+so+you+could+do
%2F%2F+something+like+`assert!%28having_fun%28%29%29`.+If+you+want+to+check+that+you+indeed+get+false%2C+you
%2F%2F+can+negate+the+result+of+what+you're+doing+using+`!`%2C+like+`assert!%28!having_fun%28%29%29`.
), [4](https://play.rust-lang.org/?code=%2F%2F+tests4.rs
%2F%2F+This+test+isn't+testing+our+function+--+make+it+do+that+in+such+a+way+that
%2F%2F+the+test+passes.+Then+write+a+second+test+that+tests+that+we+get+the+result
%2F%2F+we+expect+to+get+when+we+call+`times_two`+with+a+negative+number.
%2F%2F+No+hints%2C+you+can+do+this+%3A%29

pub+fn+times_two%28num%3A+i32%29+->+i32+{
++++num+*+2
}

%23[cfg%28test%29]
mod+tests+{
++++use+super%3A%3A*%3B

++++%23[test]
++++fn+returns_twice_of_positive_numbers%28%29+{
++++++++assert_eq!%284%2C+4%29%3B
++++}
}
) |
| Fehlerbehandlung | [9](https://doc.rust-lang.org/book/second-edition/ch09-00-error-handling.html) | [1](https://play.rust-lang.org/?code=%2F%2F+option1.rs
%2F%2F+This+example+panics+because+the+second+time+it+calls+`pop`%2C+the+`vec`
%2F%2F+is+empty%2C+so+`pop`+returns+`None`%2C+and+`unwrap`+panics+if+it's+called
%2F%2F+on+`None`.+Handle+this+in+a+more+graceful+way+than+calling+`unwrap`!
%2F%2F+Scroll+down+for+hints+%3A%29

fn+main%28%29+{
++++let+mut+list+%3D+vec![3]%3B

++++let+last+%3D+list.pop%28%29.unwrap%28%29%3B
++++println!%28"The+last+item+in+the+list+is+{%3A%3F}"%2C+last%29%3B

++++let+second_to_last+%3D+list.pop%28%29.unwrap%28%29%3B
++++println!%28"The+second-to-last+item+in+the+list+is+{%3A%3F}"%2C+second_to_last%29%3B
}

























%2F%2F+Try+using+a+`match`+statement+where+the+arms+are+`Some%28thing%29`+and+`None`.
%2F%2F+Or+set+a+default+value+to+print+out+if+you+get+`None`+by+using+the
%2F%2F+function+`unwrap_or`.
%2F%2F+Or+use+an+`if+let`+statement+on+the+result+of+`pop%28%29`+to+both+destructure
%2F%2F+a+`Some`+value+and+only+print+out+something+if+we+have+a+value!
), [2](https://play.rust-lang.org/?code=%2F%2F+result1.rs
%2F%2F+Make+this+test+pass!+Scroll+down+for+hints+%3A%29

%23[derive%28PartialEq%2CDebug%29]
struct+PositiveNonzeroInteger%28u64%29%3B

%23[derive%28PartialEq%2CDebug%29]
enum+CreationError+{
++++Negative%2C
++++Zero%2C
}

impl+PositiveNonzeroInteger+{
++++fn+new%28value%3A+i64%29+->+Result<PositiveNonzeroInteger%2C+CreationError>+{
++++++++Ok%28PositiveNonzeroInteger%28value+as+u64%29%29
++++}
}

%23[test]
fn+test_creation%28%29+{
++++assert!%28PositiveNonzeroInteger%3A%3Anew%2810%29.is_ok%28%29%29%3B
++++assert_eq!%28Err%28CreationError%3A%3ANegative%29%2C+PositiveNonzeroInteger%3A%3Anew%28-10%29%29%3B
++++assert_eq!%28Err%28CreationError%3A%3AZero%29%2C+PositiveNonzeroInteger%3A%3Anew%280%29%29%3B
}
















%2F%2F+`PositiveNonzeroInteger%3A%3Anew`+is+always+creating+a+new+instance+and+returning+an+`Ok`+result.
%2F%2F+It+should+be+doing+some+checking%2C+returning+an+`Err`+result+if+those+checks+fail%2C+and+only
%2F%2F+returning+an+`Ok`+result+if+those+checks+determine+that+everything+is...+okay+%3A%29
), [3](https://play.rust-lang.org/?code=%2F%2F+errors1.rs
%2F%2F+This+function+refuses+to+generate+text+to+be+printed+on+a+nametag+if
%2F%2F+you+pass+it+an+empty+string.+It'd+be+nicer+if+it+explained+what+the+problem
%2F%2F+was%2C+instead+of+just+sometimes+returning+`None`.+The+2nd+test+currently
%2F%2F+does+not+compile+or+pass%2C+but+it+illustrates+the+behavior+we+would+like
%2F%2F+this+function+to+have.
%2F%2F+Scroll+down+for+hints!!!

pub+fn+generate_nametag_text%28name%3A+String%29+->+Option<String>+{
++++if+name.len%28%29+>+0+{
++++++++Some%28format!%28"Hi!+My+name+is+{}"%2C+name%29%29
++++}+else+{
++++++++%2F%2F+Empty+names+aren't+allowed.
++++++++None
++++}
}

%23[cfg%28test%29]
mod+tests+{
++++use+super%3A%3A*%3B

++++%2F%2F+This+test+passes+initially+if+you+comment+out+the+2nd+test.
++++%2F%2F+You'll+need+to+update+what+this+test+expects+when+you+change
++++%2F%2F+the+function+under+test!
++++%23[test]
++++fn+generates_nametag_text_for_a_nonempty_name%28%29+{
++++++++assert_eq!%28
++++++++++++generate_nametag_text%28"Beyoncé".into%28%29%29%2C
++++++++++++Some%28"Hi!+My+name+is+Beyoncé".into%28%29%29
++++++++%29%3B
++++}

++++%23[test]
++++fn+explains_why_generating_nametag_text_fails%28%29+{
++++++++assert_eq!%28
++++++++++++generate_nametag_text%28"".into%28%29%29%2C
++++++++++++Err%28"`name`+was+empty%3B+it+must+be+nonempty.".into%28%29%29
++++++++%29%3B
++++}
}




















%2F%2F+`Err`+is+one+of+the+variants+of+`Result`%2C+so+what+the+2nd+test+is+saying
%2F%2F+is+that+`generate_nametag_text`+should+return+a+`Result`+instead+of+an
%2F%2F+`Option`.

%2F%2F+To+make+this+change%2C+you'll+need+to%3A
%2F%2F+-+update+the+return+type+in+the+function+signature+to+be+a+Result+that
%2F%2F+++could+be+the+variants+`Ok%28String%29`+and+`Err%28String%29`
%2F%2F+-+change+the+body+of+the+function+to+return+`Ok%28stuff%29`+where+it+currently
%2F%2F+++returns+`Some%28stuff%29`
%2F%2F+-+change+the+body+of+the+function+to+return+`Err%28error+message%29`+where+it
%2F%2F+++currently+returns+`None`
%2F%2F+-+change+the+first+test+to+expect+`Ok%28stuff%29`+where+it+currently+expects
%2F%2F+++`Some%28stuff%29`.
), [4](https://play.rust-lang.org/?code=%2F%2F+errors2.rs
%2F%2F+Say+we're+writing+a+game+where+you+can+buy+items+with+tokens.+All+items+cost
%2F%2F+5+tokens%2C+and+whenever+you+purchase+items+there+is+a+processing+fee+of+1
%2F%2F+token.+A+player+of+the+game+will+type+in+how+many+items+they+want+to+buy%2C
%2F%2F+and+the+`total_cost`+function+will+calculate+the+total+number+of+tokens.
%2F%2F+Since+the+player+typed+in+the+quantity%2C+though%2C+we+get+it+as+a+string--+and
%2F%2F+they+might+have+typed+anything%2C+not+just+numbers!

%2F%2F+Right+now%2C+this+function+isn't+handling+the+error+case+at+all+%28and+isn't
%2F%2F+handling+the+success+case+properly+either%29.+What+we+want+to+do+is%3A
%2F%2F+if+we+call+the+`parse`+function+on+a+string+that+is+not+a+number%2C+that
%2F%2F+function+will+return+a+`ParseIntError`%2C+and+in+that+case%2C+we+want+to
%2F%2F+immediately+return+that+error+from+our+function+and+not+try+to+multiply
%2F%2F+and+add.

%2F%2F+There+are+at+least+two+ways+to+implement+this+that+are+both+correct--+but
%2F%2F+one+is+a+lot+shorter!+Scroll+down+for+hints+to+both+ways.

use+std%3A%3Anum%3A%3AParseIntError%3B

pub+fn+total_cost%28item_quantity%3A+%26str%29+->+Result<i32%2C+ParseIntError>+{
++++let+processing_fee+%3D+1%3B
++++let+cost_per_item+%3D+5%3B
++++let+qty+%3D+item_quantity.parse%3A%3A<i32>%28%29%3B

++++Ok%28qty+*+cost_per_item+%2B+processing_fee%29
}

%23[cfg%28test%29]
mod+tests+{
++++use+super%3A%3A*%3B

++++%23[test]
++++fn+item_quantity_is_a_valid_number%28%29+{
++++++++assert_eq!%28
++++++++++++total_cost%28"34"%29%2C
++++++++++++Ok%28171%29
++++++++%29%3B
++++}

++++%23[test]
++++fn+item_quantity_is_an_invalid_number%28%29+{
++++++++assert_eq!%28
++++++++++++total_cost%28"beep+boop"%29.unwrap_err%28%29.to_string%28%29%2C
++++++++++++"invalid+digit+found+in+string"
++++++++%29%3B
++++}
}

















%2F%2F+One+way+to+handle+this+is+using+a+`match`+statement+on
%2F%2F+`item_quantity.parse%3A%3A<i32>%28%29`+where+the+cases+are+`Ok%28something%29`+and
%2F%2F+`Err%28something%29`.+This+pattern+is+very+common+in+Rust%2C+though%2C+so+there's
%2F%2F+a+`try!`+macro+that+does+pretty+much+what+you+would+make+that+match+statement
%2F%2F+do+for+you!+Take+a+look+at+this+section+of+the+Error+Handling+chapter%3A
%2F%2F+https%3A%2F%2Fdoc.rust-lang.org%2Fstable%2Fbook%2Ferror-handling.html%23the-try-macro
%2F%2F+and+give+it+a+`try!`
), [5](https://play.rust-lang.org/?code=%2F%2F+errors3.rs
%2F%2F+This+is+a+program+that+is+trying+to+use+a+completed+version+of+the
%2F%2F+`total_cost`+function+from+the+previous+exercise.+It's+not+working+though--
%2F%2F+we+can't+call+the+`try!`+macro+in+the+`main%28%29`+function!+Why+not%3F
%2F%2F+What+should+we+do+instead%3F+Scroll+for+hints!

use+std%3A%3Anum%3A%3AParseIntError%3B

fn+main%28%29+{
++++let+mut+tokens+%3D+100%3B
++++let+pretend_user_input+%3D+"8"%3B

++++let+cost+%3D+try!%28total_cost%28pretend_user_input%29%29%3B

++++if+cost+>+tokens+{
++++++++println!%28"You+can't+afford+that+many!"%29%3B
++++}+else+{
++++++++tokens+-%3D+cost%3B
++++++++println!%28"You+now+have+{}+tokens."%2C+tokens%29%3B
++++}
}

pub+fn+total_cost%28item_quantity%3A+%26str%29+->+Result<i32%2C+ParseIntError>+{
++++let+processing_fee+%3D+1%3B
++++let+cost_per_item+%3D+5%3B
++++let+qty+%3D+try!%28item_quantity.parse%3A%3A<i32>%28%29%29%3B

++++Ok%28qty+*+cost_per_item+%2B+processing_fee%29
}


















%2F%2F+Since+the+`try!`+macro+returns+an+`Err`+early+if+the+thing+it's+trying+to
%2F%2F+do+fails%2C+you+can+only+use+the+`try!`+macro+in+functions+that+have+a
%2F%2F+`Result`+as+their+return+type.

%2F%2F+The+error+that+you+get+if+you+run+this+code+is%3A

%2F%2F+```
%2F%2F+error%3A+mismatched+types%3A
%2F%2F+expected+`%28%29`%2C
%2F%2F+found+`std%3A%3Aresult%3A%3AResult<_%2C+_>`
%2F%2F+```

%2F%2F+which+is+saying+that+the+expected+return+type+of+the+`main`+function+is
%2F%2F+the+empty+tuple%2C+but+we+tried+to+return+a+`Result`--+and+that's+happening
%2F%2F+in+the+implementation+of+`try!`.+The+`main`+function+never+has+a+return+type%2C
%2F%2F+so+we+have+to+use+another+way+of+handling+a+`Result`+within+`main`.

%2F%2F+Decide+what+we+should+do+if+`pretend_user_input`+has+a+string+value+that+does
%2F%2F+not+parse+to+an+integer%2C+and+implement+that+instead+of+calling+the+`try!`
%2F%2F+macro.
), [6](https://play.rust-lang.org/?code=%2F%2F+errorsn.rs
%2F%2F+This+is+a+bigger+error+exercise+than+the+previous+ones!
%2F%2F+You+can+do+it!+%3A%29
%2F%2F
%2F%2F+Edit+the+`read_and_validate`+function+so+that+it+compiles+and
%2F%2F+passes+the+tests...+so+many+things+could+go+wrong!
%2F%2F
%2F%2F+-+Reading+from+stdin+could+produce+an+io%3A%3AError
%2F%2F+-+Parsing+the+input+could+produce+a+num%3A%3AParseIntError
%2F%2F+-+Validating+the+input+could+produce+a+CreationError+%28defined+below%29
%2F%2F
%2F%2F+How+can+we+lump+these+errors+into+one+general+error%3F+That+is%2C+what
%2F%2F+type+goes+where+the+question+marks+are%2C+and+how+do+we+return
%2F%2F+that+type+from+the+body+of+read_and_validate%3F
%2F%2F
%2F%2F+Scroll+down+for+hints+%3A%29

use+std%3A%3Aerror%3B
use+std%3A%3Afmt%3B
use+std%3A%3Aio%3B

%2F%2F+PositiveNonzeroInteger+is+a+struct+defined+below+the+tests.
fn+read_and_validate%28b%3A+%26mut+io%3A%3ABufRead%29+->+Result<PositiveNonzeroInteger%2C+%3F%3F%3F>+{
++++let+mut+line+%3D+String%3A%3Anew%28%29%3B
++++b.read_line%28%26mut+line%29%3B
++++let+num%3A+i64+%3D+line.trim%28%29.parse%28%29%3B
++++let+answer+%3D+PositiveNonzeroInteger%3A%3Anew%28num%29%3B
++++answer
}

%2F%2F+This+is+a+test+helper+function+that+turns+a+%26str+into+a+BufReader.
fn+test_with_str%28s%3A+%26str%29+->+Result<PositiveNonzeroInteger%2C+Box<error%3A%3AError>>+{
++++let+mut+b+%3D+io%3A%3ABufReader%3A%3Anew%28s.as_bytes%28%29%29%3B
++++read_and_validate%28%26mut+b%29
}

%23[test]
fn+test_success%28%29+{
++++let+x+%3D+test_with_str%28"42\n"%29%3B
++++assert_eq!%28PositiveNonzeroInteger%2842%29%2C+x.unwrap%28%29%29%3B
}

%23[test]
fn+test_not_num%28%29+{
++++let+x+%3D+test_with_str%28"eleven+billion\n"%29%3B
++++assert!%28x.is_err%28%29%29%3B
}

%23[test]
fn+test_non_positive%28%29+{
++++let+x+%3D+test_with_str%28"-40\n"%29%3B
++++assert!%28x.is_err%28%29%29%3B
}

%23[test]
fn+test_ioerror%28%29+{
++++struct+Broken%3B
++++impl+io%3A%3ARead+for+Broken+{
++++++++fn+read%28%26mut+self%2C+_buf%3A+%26mut+[u8]%29+->+io%3A%3AResult<usize>+{
++++++++++++Err%28io%3A%3AError%3A%3Anew%28io%3A%3AErrorKind%3A%3ABrokenPipe%2C+"uh-oh!"%29%29
++++++++}
++++}
++++let+mut+b+%3D+io%3A%3ABufReader%3A%3Anew%28Broken%29%3B
++++assert!%28read_and_validate%28%26mut+b%29.is_err%28%29%29%3B
++++assert_eq!%28"uh-oh!"%2C+read_and_validate%28%26mut+b%29.unwrap_err%28%29.to_string%28%29%29%3B
}

%23[derive%28PartialEq%2CDebug%29]
struct+PositiveNonzeroInteger%28u64%29%3B

impl+PositiveNonzeroInteger+{
++++fn+new%28value%3A+i64%29+->+Result<PositiveNonzeroInteger%2C+CreationError>+{
++++++++if+value+%3D%3D+0+{
++++++++++++Err%28CreationError%3A%3AZero%29
++++++++}+else+if+value+<+0+{
++++++++++++Err%28CreationError%3A%3ANegative%29
++++++++}+else+{
++++++++++++Ok%28PositiveNonzeroInteger%28value+as+u64%29%29
++++++++}
++++}
}

%23[test]
fn+test_positive_nonzero_integer_creation%28%29+{
++++assert!%28PositiveNonzeroInteger%3A%3Anew%2810%29.is_ok%28%29%29%3B
++++assert_eq!%28Err%28CreationError%3A%3ANegative%29%2C+PositiveNonzeroInteger%3A%3Anew%28-10%29%29%3B
++++assert_eq!%28Err%28CreationError%3A%3AZero%29%2C+PositiveNonzeroInteger%3A%3Anew%280%29%29%3B
}

%23[derive%28PartialEq%2CDebug%29]
enum+CreationError+{
++++Negative%2C
++++Zero%2C
}

impl+fmt%3A%3ADisplay+for+CreationError+{
++++fn+fmt%28%26self%2C+f%3A+%26mut+fmt%3A%3AFormatter%29+->+fmt%3A%3AResult+{
++++++++f.write_str%28%28self+as+%26error%3A%3AError%29.description%28%29%29
++++}
}

impl+error%3A%3AError+for+CreationError+{
++++fn+description%28%26self%29+->+%26str+{
++++++++match+*self+{
++++++++++++CreationError%3A%3ANegative+%3D>+"Negative"%2C
++++++++++++CreationError%3A%3AZero+%3D>+"Zero"%2C
++++++++}
++++}
}

%2F%2F+First+hint%3A+To+figure+out+what+type+should+go+where+the+%3F%3F%3F+is%2C+take+a+look
%2F%2F+at+the+test+helper+function+`test_with_str`%2C+since+it+returns+whatever
%2F%2F+`read_and_validate`+returns+and`test_with_str`+has+its+signature+fully
%2F%2F+specified.

%2F%2F+Next+hint%3A+There+are+three+places+in+`read_and_validate`+that+we+call+a
%2F%2F+function+that+returns+a+`Result`+%28that+is%2C+the+functions+might+fail%29.
%2F%2F+Wrap+those+calls+in+a+`try!`+macro+call+so+that+we+return+immediately+from
%2F%2F+`read_and_validate`+if+those+function+calls+fail.

%2F%2F+Another+hint%3A+under+the+hood%2C+the+`try!`+macro+calls+`From%3A%3Afrom`
%2F%2F+on+the+error+value+to+convert+it+to+a+boxed+trait+object%2C+a+Box<error%3A%3AError>%2C
%2F%2F+which+is+polymorphic--+that+means+that+lots+of+different+kinds+of+errors
%2F%2F+can+be+returned+from+the+same+function+because+all+errors+act+the+same
%2F%2F+since+they+all+implement+the+`error%3A%3AError`+trait.
%2F%2F+Check+out+this+section+of+the+book%3A
%2F%2F+https%3A%2F%2Fdoc.rust-lang.org%2Fstable%2Fbook%2Ferror-handling.html%23standard-library-traits-used-for-error-handling

%2F%2F+Another+another+hint%3A+Note+that+because+the+`try!`+macro+returns
%2F%2F+the+*unwrapped*+value+in+the+`Ok`+case%2C+if+we+want+to+return+a+`Result`+from
%2F%2F+`read_and_validate`+for+*its*+success+case%2C+we'll+have+to+rewrap+a+value
%2F%2F+that+we+got+from+the+return+value+of+a+`try!`+call+in+an+`Ok`--+this+will
%2F%2F+look+like+`Ok%28something%29`.

%2F%2F+Another+another+another+hint%3A+`Result`s+must+be+"used"%2C+that+is%2C+you'll
%2F%2F+get+a+warning+if+you+don't+handle+a+`Result`+tha+you+get+in+your
%2F%2F+function.+Read+more+about+that+in+the+`std%3A%3Aresult`+module+docs%3A
%2F%2F+https%3A%2F%2Fdoc.rust-lang.org%2Fstd%2Fresult%2F%23results-must-be-used
) |
| Generics | [10](https://doc.rust-lang.org/book/second-edition/ch10-00-generics.html) | [1](http://exercism.io/exercises/rust/sublist/readme), [2\*](http://exercism.io/exercises/rust/binary-search/readme) |
| Closures | [13.1](https://doc.rust-lang.org/book/second-edition/ch13-01-closures.html) | [1](http://exercism.io/exercises/rust/accumulate/readme) |
| Iterators | [13.2](https://doc.rust-lang.org/book/second-edition/ch13-02-iterators.html) | [2](https://play.rust-lang.org/?code=%2F%2F+iterator3.rs
%2F%2F+This+is+a+bigger+exercise+than+most+of+the+others!+You+can+do+it!
%2F%2F+Here+is+your+mission%2C+should+you+choose+to+accept+it%3A
%2F%2F+1.+Complete+the+divide+function+to+get+the+first+four+tests+to+pass
%2F%2F+2.+Uncomment+the+last+two+tests+and+get+them+to+pass+by+filling+in
%2F%2F++++values+for+`x`+using+`division_results`.
%2F%2F+Scroll+down+for+a+minor+hint+for+part+2%2C+and+scroll+down+further+for
%2F%2F+a+major+hint.
%2F%2F+Have+fun+%3A-%29

%23[derive%28Debug%2C+PartialEq%2C+Eq%29]
pub+enum+DivisionError+{
++++NotDivisible%28NotDivisibleError%29%2C
++++DivideByZero%2C
}

%23[derive%28Debug%2C+PartialEq%2C+Eq%29]
pub+struct+NotDivisibleError+{
++++dividend%3A+i32%2C
++++divisor%3A+i32%2C
}

%2F%2F+This+function+should+calculate+`a`+divided+by+`b`+if+`a`+is
%2F%2F+evenly+divisible+by+b.
%2F%2F+Otherwise%2C+it+should+return+a+suitable+error.
pub+fn+divide%28a%3A+i32%2C+b%3A+i32%29+->+Result<i32%2C+DivisionError>+{
}

%23[cfg%28test%29]
mod+tests+{
++++use+super%3A%3A*%3B

++++%2F%2F+Tests+that+verify+your+`divide`+function+implementation
++++%23[test]
++++fn+test_success%28%29+{
++++++++assert_eq!%28divide%2881%2C+9%29%2C+Ok%289%29%29%3B
++++}

++++%23[test]
++++fn+test_not_divisible%28%29+{
++++++++assert_eq!%28
++++++++++++divide%2881%2C+6%29%2C
++++++++++++Err%28DivisionError%3A%3ANotDivisible%28NotDivisibleError{
++++++++++++++++dividend%3A+81%2C
++++++++++++++++divisor%3A+6
++++++++++++}%29%29
++++++++%29%3B
++++}

++++%23[test]
++++fn+test_divide_by_0%28%29+{
++++++++assert_eq!%28divide%2881%2C+0%29%2C+Err%28DivisionError%3A%3ADivideByZero%29%29%3B
++++}

++++%23[test]
++++fn+test_divide_0_by_something%28%29+{
++++++++assert_eq!%28divide%280%2C+81%29%2C+Ok%280%29%29%3B
++++}

++++%2F%2F+Iterator+exercises+using+your+`divide`+function
++++%2F*
++++%23[test]
++++fn+result_with_list%28%29+{
++++++++let+numbers+%3D+vec![27%2C+297%2C+38502%2C+81]%3B
++++++++let+division_results+%3D+numbers.into_iter%28%29.map%28|n|+divide%28n%2C+27%29%29%3B
++++++++let+x+%2F%2F...+Fill+in+here!
++++++++assert_eq!%28format!%28"{%3A%3F}"%2C+x%29%2C+"Ok%28[1%2C+11%2C+1426%2C+3]%29"%29%3B
++++}

++++%23[test]
++++fn+list_of_results%28%29+{
++++++++let+numbers+%3D+vec![27%2C+297%2C+38502%2C+81]%3B
++++++++let+division_results+%3D+numbers.into_iter%28%29.map%28|n|+divide%28n%2C+27%29%29%3B
++++++++let+x+%2F%2F...+Fill+in+here!
++++++++assert_eq!%28format!%28"{%3A%3F}"%2C+x%29%2C+"[Ok%281%29%2C+Ok%2811%29%2C+Ok%281426%29%2C+Ok%283%29]"%29%3B
++++}
++++*%2F
}






































%2F%2F+Minor+hint%3A+In+each+of+the+two+cases+in+the+match+in+main%2C+you+can+create+x+with+either+a+'turbofish'+or+by+hinting+the+type+of+x+to+the+compiler.+You+may+try+both.



























%2F%2F+Major+hint%3A+Have+a+look+at+the+Iter+trait+and+at+the+explanation+of+its+collect+function.+Especially+the+part+about+Result+is+interesting.
), [3](https://play.rust-lang.org/?code=%2F%2F+iterators4.rs

pub+fn+factorial%28num%3A+u64%29+->+u64+{
++++%2F%2F+Complete+this+function+to+return+factorial+of+num
++++%2F%2F+Do+not+use%3A
++++%2F%2F+-+return
++++%2F%2F+For+extra+fun+don't+use%3A
++++%2F%2F+-+imperative+style+loops+%28for%2C+while%29
++++%2F%2F+-+additional+variables
++++%2F%2F+For+the+most+fun+don't+use%3A
++++%2F%2F+-+recursion
++++%2F%2F+Scroll+down+for+hints.
}

%23[cfg%28test%29]
mod+tests+{
++++use+super%3A%3A*%3B

++++%23[test]
++++fn+factorial_of_1%28%29+{
++++++++assert_eq!%281%2C+factorial%281%29%29%3B
++++}
++++%23[test]
++++fn+factorial_of_2%28%29+{
++++++++assert_eq!%282%2C+factorial%282%29%29%3B
++++}

++++%23[test]
++++fn+factorial_of_4%28%29+{
++++++++assert_eq!%2824%2C+factorial%284%29%29%3B
++++}
}

























%2F%2F+In+an+imperative+language+you+might+write+a+for+loop+to+iterate+through
%2F%2F+multiply+the+values+into+a+mutable+variable.+Or+you+might+write+code+more
%2F%2F+functionally+with+recursion+and+a+match+clause.+But+you+can+also+use+ranges
%2F%2F+and+iterators+to+solve+this+in+rust.
) |
| Heap allocation | [15.1](https://doc.rust-lang.org/book/second-edition/ch15-01-box.html) | [1](http://exercism.io/exercises/rust/simple-linked-list/readme) |



