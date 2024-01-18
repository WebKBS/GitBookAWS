# Setting

AWS ISM 대시보드로 이동한다.

## 사용자 생성

아래와 같이 화면이 나오는데 사용자 아래 0을 클릭한다. 그러면 사용자 페이지로 이동한다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 21.32.32.png" alt=""><figcaption></figcaption></figure>

사용자 페이지에서 사용자 생성을 클릭한다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 21.34.00.png" alt=""><figcaption></figcaption></figure>

사용자 이름 설정이 나오는데 사용자 이름을 설정하고 다음을 누른다.



그룹을 생성한적이 없기때문에 비어있다. 그룹을 만들어야한다.

그룹 생성버튼을 누르자.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 21.35.34.png" alt=""><figcaption></figcaption></figure>

아래와 같이 모달창이 나오는데, 사용자 그룹 이름을 설정하고 권한 정책에서 AmazonS3FullAccess 를 검색한뒤

AmazonS3FullAccess 앞 체크박스를 클릭한뒤 사용자 그룹 생성을 클릭한다.

{% hint style="warning" %}
AmazonS3FullAccess는 AWS S3의 권한을 설정하기 위함이다.

사용하는 프로그램의 정책에 따라 다르다.

AWS S3 하나만 사용하기 위함이니 AmazonS3FullAccess를 체크한다.
{% endhint %}

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 21.39.41.png" alt=""><figcaption></figcaption></figure>

그룹을 생성하고나면 아래와같이 그룹이름이 생성된 것을 볼 수 있다. \
체크박스에 체크를하고 다음 버튼을 누르자.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 21.43.56.png" alt=""><figcaption></figcaption></figure>

다음을 누르면 사용자 생성 페이지의 정보가 나타난다.

다음 사용자 생성 버튼을 누르자.

사용자가 생성된것을 확인 할 수 있다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 21.47.16.png" alt=""><figcaption></figcaption></figure>

사용자 이름을 클릭하면 아래처럼 사용자의 정보를 볼수 있다.

&#x20;이제 액세스 키를 만들어야한다. 액세스 키 만들기를 클릭한다.

## 액세스 키 생성

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 21.48.31.png" alt=""><figcaption></figcaption></figure>

액세스 키에 대한 내용이 아래와 같이 나온다. 기타를 누르고 다음을 누른다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 21.51.23.png" alt=""><figcaption></figcaption></figure>

다음 페이지로 넘어가면 설명 태그값을 입력하라고 나오는데, 이는 무시하고 액세스 키 만들기를 클릭한다.

아래와 같이 액세스 키가 생성 된다.

{% hint style="danger" %}
알림에도 떠 있듯이 액세스키는 현재 페이지를 닫거나 완료를 누르면 다시 보거나 다운로드 할수 없다.

그러나 다시 설정해서 새로운 키를 생성후 사용할 수 있다.
{% endhint %}

액세스 키와 비밀 액세스 키를 따로 복사해서 노트해 둔다.

필요시 파일을 다운로드 할 수도있다.

{% hint style="warning" %}
액세스 키를 자주 변경하기 싫다면 .csv 파일을 다운로드 받아 재사용 가능하나, 보안에 혹시나 취약할수 있으니 선택은 본인 몫으로.
{% endhint %}

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 21.55.17.png" alt=""><figcaption></figcaption></figure>

완료 버튼을 누르면 액세스키가 설정된다.
