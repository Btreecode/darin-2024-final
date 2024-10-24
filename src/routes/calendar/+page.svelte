<div class="flex justify-center">
    <button class="btn btn-sm btn-info color:grey">prev</button>
    <div>2024/1/1</div>
    <button class="btn btn-sm btn-info">next</button>
</div>

<div class="border-2 p-2 inline-grid grid-cols-7 cal">
    <div>1</div>
    <div>2</div>
    <div>3</div>
    <div>4</div>
    <div>5</div>
    <div class="circle">6</div>
    <div class="circle">7</div>
    <div class="circle">8</div>
    <div class="circle">9</div>
    <div>10</div>
    <div>11</div>
    <div>12</div>
    <div>13</div>
    <div>14</div>
    <div>15</div>
    <div>16</div>
    <div>17</div>
    <div>18</div>
    <div>19</div>
    <div>20</div>
    <div>21</div>
    <div>22</div>
    <div>23</div>
    <div>24</div>
    <div>25</div>
    <div>26</div>
    <div>27</div>
    <div>28</div>
    <div>29</div>
    <div>30</div>
    <div>31</div>
</div>

<div>
    달력 회색 동그라미 없애고 출석한날에만 회색동그라미
    prev 이랑 next는 버튼 검정으로하고 글자색 하얀색
    날짜 텍스트 굵기
</div>

<style>
.cal div {
    width: 30px;
    height: 30px;
    background: rgba(234, 232, 232, 0.832);
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 20px;
}

.cal .circle {
    background: rgb(0, 0, 0);
    text-decoration-color: white;
}
</style>