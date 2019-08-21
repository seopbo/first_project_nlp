# 윈도우 용 mecab 설치

#### 1. https://github.com/Pusnow/mecab-ko-msvc/releases/tag/release-0.9.2-msvc-3 
윈도우에서 메캅을 실행할 수 있는 파일 설치. 우선 다운로드 하자

mecab-ko-msvc-x64.zip 또는 mecab-ko-msvc-x86.zip

윈도우 32/64bit 에 따라서 다운로드한후
c:mecab 에 압축을 푼다.

아래처럼 파일이 풀려야 함다.
C:\mecab\mecab.exe
C:\mecab\.........

#### 2. https://github.com/Pusnow/mecab-ko-dic-msvc/releases/tag/mecab-ko-dic-2.1.1-20180720-msvc
여기서 메캅 사전 설치. 다운로드 해서 mecab 폴더에 압축을 푼다.

mecab-ko-dic-msvc.zip

72 메가라서 다운이 안될까봐 합께 올려놓고

C:\mecab\mecab-ko-dic
C:\mecab\tools
C:\mecab\user-dic

이런 형식으로 압축을 푼다.

#### 3. https://github.com/Pusnow/mecab-python-msvc/releases/tag/mecab_python-0.996_ko_0.9.2_msvc-2
파이썬 휠로 파이썬메캅설치. 자신의 맞는 파이썬 버전에 맞는 그리고 윈도우 32/64 bit 에 맞춰서 다운로드 하여 설치

파이썬 3.6 에 윈도우 64비트 설치 예시

pip install mecab_python-0.996_ko_0.9.2_msvc-cp36-cp36m-win_amd64.whl

#### 4. 사용예시
exercise 폴더의 eda_winmecab_example.ipynb 파일의 14번째 셀 참조

```python
# 문장을 형태소기준으로 split 윈도우일때 하는 방법 추가
import MeCab
mecab_tagger = MeCab.Tagger()

def split_morph(sentence):
    return [
        node.split('\t')[0]
        for node in mecab_tagger.parse(sentence).split('\n')
    ][:-2]

print(example_sentence, split_morph(example_sentence))

```
