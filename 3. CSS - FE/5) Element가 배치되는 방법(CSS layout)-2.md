# 5) Element가 배치되는 방법(CSS layout)-2

**들어가기 전에**

CSS의 배치를 위해서는 중요한 여러 가지 개념을 알고 있어야 합니다.

그중에서 block과 inline의 차이 그리고 position 속성을 이해해야 합니다.

또한, 많이 사용되고 있는 float의 성질도 알아둘 필요가 있습니다.

**학습 목표**

1) layout의 방식에 대해서 이해합니다.

**핵심 개념**

- 박스 모델 (Box model)
- margin
- border
- padding
- position

**엘리먼트의 크기는 부모의 크기가 기본.**

block엘리먼트의 크기는 기본적으로는 부모의 크기만큼을 가집니다.
예를들어 width:100%는 부모의 크기만큼을 다 갖는 것과 같습니다.

**box-sizing과 padding**

padding 속성을 늘리면 엘리먼트의 크기가 달라질 수 있습니다.

box-sizing 속성으로 이를 컨트롤 할 수 있습니다.

box-sizing 속성을 border-box로 설정하면 엘리먼트의 크기를 고정하면서 padding 값만 늘릴 수 있습니다.

**layout 구현방법은?**

전체 레이아웃은 float를 잘 사용해서 2단, 3단 컬럼 배치를 구현합니다.

최근에는 css-grid나 flex 속성 등 layout을 위한 속성을 사용하기 시작했으며 브라우저 지원범위를 확인해서 사용하도록 합니다.

특별한 위치에 배치하기 위해서는 position absolute를 사용하고, 기준점을 relative로 설정합니다.

네비게이션과 같은 엘리먼트는 block 엘리먼트를 inline-block으로 변경해서 가로로 배치하기도 합니다.

엘리먼트안의 텍스트의 간격과 다른 엘리먼트간의 간격은 padding과 margin 속성을 잘 활용해서 위치시킵니다.
