# typescript
tsc&amp;nest_study

1. typescript 설치 방법
**- npm install -g typescript**
- 파일명.ts 파일 생성

[typescript data_types]
- number
- string
- boolean
- null
- undefined
- any (이것도 저것도 아닌 다른 타입)

ex) 
let a: number = 3
a = "hi" // number로 선언했는데, string 값 넣을 수 없음

let c:any = 4

c = "asdfasdf" // any는 아무타입이 가능하지만, 사용 지양

let d:number | string = "asdfsda" // type 2개 지정 가능
d = 3

let e:string[] = ['apple', 'mango'] // 배열시 let a:string[] = ['a','b'] 식으로 가능

function addNumber(a:number, b:number): number { // 출력값도 number값으로 지정
  return a + b
  }
  addNumber(1, 2)

2. typescript 실행 방법
- tsc 파일명.ts
- 파일명.js 파일 자동으로 생성됨
- node 파일명.js 하면 끝

3. typescript에서 javascript변환하기 위한 tsconfig.json 생성
//tsconfig.json
{
    "compilerOptions": {
        "outDir": "dist", // 어떤 폴더에 넣을지 지정
        "target": "es6",
        "module": "commonjs",
        "lib": ["es6"],

        "sourceMap": true
    },
}

- ctrl + shift + b 누른 후 --> tsc:build - tsconfig.json 클릭
*  Executing task: tsc -p "c:\Users\Sanghyun Yun\Desktop\js_ts_node_nest\tsconfig.json" 

*  Terminal will be reused by tasks, press any key to close it. 
이렇게 뜨면 정상적으로 실행. dist 폴더도 자동으로 생성됨

---

