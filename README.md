# ml5.js 활용 컴퓨터 그래픽스 개별 과제
## 머신러닝 + 자바스크립트 : P5js와 ML5js를 이용한 개, 고양이 품종 알아내기

 ml5.js 활용 컴퓨터 그래픽스 개별 과제 안내서

<details>
 
 <summary>개별 과제 안내서 상세 내용</summary>
1. 개요



본 과제는 ml5.js 라이브러리를 활용하여 컴퓨터 그래픽스 효과를 구현하는 개별 과제입니다. ml5.js는 웹 브라우저에서 머신러닝 모델을 실행할 수 있도록 지원하는 JavaScript 라이브러리입니다. 

 

이 과제를 통해 학생들은 ml5.js 라이브러리의 다양한 기능을 활용하여 창의적인 컴퓨터 그래픽스 효과를 만들고, 머신러닝 기술과 컴퓨터 그래픽스의 결합을 경험하며, 문제 해결 능력과 창의력을 향상시킬 수 있습니다.

 

2. 목표

 

* ml5.js 라이브러리의 다양한 기능 활용법 익히기

* 창의적이고 흥미로운 컴퓨터 그래픽스 효과 구현

* 머신러닝 기술과 컴퓨터 그래픽스의 결합 경험

* 문제 해결 능력 및 창의력 향상

 

3. 과제 내용

 

1. 프로젝트 아이디어 선정:

 

    * ml5.js 라이브러리가 제공하는 다양한 기능들을 활용하여 창의적이고 흥미로운 컴퓨터 그래픽스 효과 아이디어를 선택합니다.

    * 예시:

        * 이미지 변형: 이미지 왜곡, 모자이크 효과, 스타일 변환

        * 애니메이션: 이미지 애니메이션, 3D 모델 애니메이션

        * 상호 작용: 웹캠 입력 활용, 터치 입력 활용

        * 창의적인 효과: 예술적 표현, 게임 효과

 

2. 프로젝트 계획 수립:

 

    * 선정된 아이디어를 구체적인 프로젝트 계획으로 작성합니다.

    * 프로젝트 계획에는 다음 내용이 포함되어야 합니다:

        * 프로젝트 목표 및 효과

        * 사용할 ml5.js 라이브러리 기능

        * 필요한 데이터 및 데이터 수집 방법

        * 개발 환경 및 도구

        * 예상 소요 시간

        * 평가 기준

 

3. 프로젝트 개발:

 

    * 프로젝트 계획에 따라 웹 기반 컴퓨터 그래픽스 애플리케이션을 개발합니다.

    * ml5.js 라이브러리의 다양한 기능을 활용하여 아이디어를 구현합니다.

    * 코드 작성 시 코드 가독성, 효율성, 보안성을 고려합니다.

 

4. 프로젝트 평가:

 

    * 완성된 웹 기반 컴퓨터 그래픽스 애플리케이션을 평가합니다.

    * 평가 기준은 다음과 같습니다:

        * 효과 완성도 및 시각적 매력

        * 코드 품질 및 디자인

        * 창의성 및 흥미도

        * 사용자 편의성 및 접근성

        * 발표 및 문서 작성

 

4. 평가 기준

 

* 효과 완성도 및 시각적 매력 (40%)

* 코드 품질 및 디자인 (30%)

* 창의성 및 흥미도 (20%)

* 사용자 편의성 및 접근성 (10%)

 

5. 참고 자료

 

* ml5.js 공식 웹사이트: [https://ml5js.org/](https://ml5js.org/)

* ml5.js 튜토리얼: [https://learn.ml5js.org/](https://learn.ml5js.org/)

* ml5.js 예제 코드: [https://github.com/ml5js](https://github.com/ml5js)

* 컴퓨터 그래픽스 관련 온라인 강좌 및 자료

 

6. 추가 정보

 

* 본 과제는 학습 목적이며, 상업적 목적으로 사용될 수 없습니다.

* 개인 정보 보호에 유의하여 작업해야 합니다.

* 궁금한 점은 담당 교수에게 문의하십시오.

 

7. 성공적인 개별 과제를 위한 팁

 

* 명확한 목표 설정

* 철저한 계획 수립

* 적극적인 정보 검색 및 학습

* 지속적인 노력 및 문제 해결 능력

* 창의적 사고방식 및 아이디어 발굴

* 적절한 도구 및 라이브러리 활용

* 코드

 

[제출]

1. github에 올린다. 링크를 제출한다.

2. 작성소감도 github에 올린다.
</details>

### index.html 코드

```
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- 문서 설정 -->
    <meta charset="UTF-8"> <!-- 문자 인코딩 설정 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- 반응형 뷰포트 설정 -->
    <title>Document</title> <!-- 문서 제목 -->

    <!-- 외부 라이브러리 및 스타일 -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script> <!-- p5.js 라이브러리 -->
    <script src="https://unpkg.com/ml5@0.3.1/dist/ml5.min.js"></script> <!-- ml5.js 머신러닝 라이브러리 -->
    <style>
        body {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
        } <!-- body 스타일 설정 -->

        #files {
            margin: 10px;
        } <!-- 파일 입력 요소 스타일 설정 -->
        #preview {
            width: 500px;
            height: 500px;
            overflow: hidden;
        } <!-- 미리보기 이미지 스타일 설정 -->

        img {
            object-fit: cover;
        } <!-- 이미지 스타일 설정 -->

        #defaultCanvas0{
            display: none;
        } <!-- 기본 캔버스 숨김 -->
        .result{
            width: 500px;
            text-align: left;
            margin-top: 16px;
            font-size: 18px;
        } <!-- 결과 텍스트 스타일 설정 -->
    </style>
</head>
<body>

    <!-- 페이지 제목 -->
    <h1>머신러닝 Example : ML5.js를 개, 고양이 품종 알아 보기</h1>

    <!-- 사용자가 자신의 사진을 선택할 수 있는 파일 입력 요소 -->
    <p>분석할 이미지를 선택해 주세요.</p>
    <input type='file' id="files" onchange="readURL(this);" />
    <!-- 이미지를 미리보기할 요소 -->
    <img id="preview" src="images/cat.jpg" alt="your image" />    

    <!-- 사용자 정의 스크립트 -->
    <script src="sketch.js"></script>
    
</body>
</html>

```
### sketch.js  코드

```
let classifier; // 변수 classifier를 선언하여 ml5.imageClassifier('MobileNet')으로 초기화할 예정입니다.
let img; // 변수 img를 선언하여 이미지를 저장할 예정입니다.

function readURL(input) {
    // .result 클래스를 가진 요소가 존재한다면 제거합니다.
    if(document.querySelector(".result")){
        document.querySelector(".result").remove();
    }

    // 사용자가 파일을 선택했고, 선택한 파일이 존재한다면 실행합니다.
    if (input.files && input.files[0]) {
        var reader = new FileReader(); // FileReader 객체를 생성합니다.
        reader.onload = function (e) {
            classifier = ml5.imageClassifier('MobileNet'); // MobileNet 모델을 사용하여 이미지 분류기를 초기화합니다.
            img = loadImage(e.target.result); // 선택한 이미지를 로드합니다.
            classifier.classify(img, gotResult); // 분류기를 사용하여 이미지를 분류하고 결과를 콜백 함수 gotResult에 전달합니다.
            document.getElementById('preview').src = e.target.result; // 선택한 이미지를 미리보기에 표시합니다.
        };
        reader.readAsDataURL(input.files[0]); // 파일을 읽어 데이터 URL로 변환합니다.
    }
}

// function preload(){
//     classifier = ml5.imageClassifier('MobileNet');
//     img = loadImage('images/cat3.jpg');
// }

function setup(){
    // createCanvas(400, 400);
    // classifier.classify(img, gotResult);
    // image(img, 0, 0);
}

// 분류 결과가 도착했을 때 실행되는 콜백 함수입니다.
function gotResult(error, results){
    if(error){ // 오류가 발생했을 경우 오류를 콘솔에 기록합니다.
        console.log(error);
    } else {
        //console.log(results);
        var newDiv = document.createElement("div"); // 새로운 div 요소를 생성합니다.
        newDiv.classList.add("result"); // 생성한 div에 'result' 클래스를 추가합니다.
        var newText = document.createTextNode('Label : ' + results[0].label + ' / Confidence : ' + nf(results[0].confidence, 0, 2)); // 분류 결과를 텍스트로 만듭니다.
        newDiv.appendChild(newText); // 새로운 텍스트를 생성한 div에 추가합니다.
        document.body.insertBefore(newDiv, document.getElementById("preview").nextSibling); // 새로운 div를 삽입합니다.
    }
}

```
![이미지_130](https://github.com/rex6928/Computer-Graphic/assets/162276764/c00b1dce-a374-4f43-8868-bb94f2700d69)






















