### [pytest](https://pytest.org) framework
  * 언제 쓸까?
    * 테스트 함수를 미리 구축해 놓은 상태에서, 모듈의 코드를 수정했을 때 `간단하게` 테스트 함수를 실행할 수 있게 해 준다. 

### 설치

    pip install -U pytest

### 사용방법
현재 위치에서 pytest를 실행하면 아래에 기술한 패턴의 파일 및 함수를 찾아서 테스트를 수행한다.
  * 파일 이름 패턴: test_*.py 혹은 *_test.py
  * 함수 이름 패턴: def test_함수이름

### 전형적인 사용 예
test_out.py
```python
def test_A():
  import torch
  ref = torch.load('ref.pt')
  dev = torch.load('dev.pt')
  ref.allclose(dev, rtol=1e-05, atol=0)
```
Command line
```bash
home$ cd test_dir
test_dir$ pytest
```
