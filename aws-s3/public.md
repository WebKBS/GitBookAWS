# Public 설정

파일을 업로드 하면 업로드된 파일을 볼 수 있다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 17.28.41.png" alt=""><figcaption></figcaption></figure>

해당 파일을 클릭하면 파일 정보를 볼수 있다.&#x20;

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 17.30.38.png" alt=""><figcaption></figcaption></figure>

객체 URL을 클릭하면 에러 메세지가 나타난다.

이것은 이전에 default 설정으로 인해, 외부 공유를 하지 않았기 때문에 발생한다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 17.31.39.png" alt=""><figcaption></figcaption></figure>

## 권한 탭에서 생성한 버킷을 Public으로 변경.

만들어진 버킷으로 들어와서 권한 탭을 누른다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 17.26.27.png" alt=""><figcaption></figcaption></figure>

권한 탭을 살펴보면 모든 퍼블릭 엑세스 차단이라는 문구를 볼수 있다. 비공개 상태라는 뜻이다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 17.35.12.png" alt=""><figcaption></figcaption></figure>

오른쪽 끝 부분에 편집 버튼이 있다. 편집을 누른다.



아래 모든 퍼블릭 엑세스 차단을 해제 한후 변경사항을 저장한다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 17.40.23.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
하지만 아직 이미지를 볼수 없다. 정책 설정을 해야한다.
{% endhint %}

### 정책 설정

권한 페이지의 아래에 보면  "버킷 정책"이라는 것이 있다. 편집 버튼을 누른다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 18.08.11.png" alt=""><figcaption></figcaption></figure>

편집을 클릭한후 정책 예제를 살펴 볼수있다. 회사나, 개인이나 정책에 맞는 것을 사용하면 되나, 이번 내용에서는 아래 코드를 입력한다.

{% hint style="danger" %}
이것은 모두가 접근할수 있는 공개 퍼블릭 정책이다. 중요한 데이터를 저장해서는 안된다.
{% endhint %}

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicRead",
            "Effect": "Allow",
            "Principal": "*",
            "Action": [
                "s3:GetObject",
                "s3:GetObjectVersion"
            ],
            "Resource": [
                "arn:aws:s3:::DOC-EXAMPLE-BUCKET/*" // 여기는 내 퍼킷 ARN 마지막 /* 반드시 있어야함
            ]
        }
    ]
}
```



정책 란에 위 코드를 입력해주고 아래와 같이 Resource 부분에 나의 버킷 ARN을 추가해준다.

{% hint style="danger" %}
중요!! 매우중요. 문자열 마지막의 /\* 는 반드시 있어야한다!

만약에 없다면 변경사항저장시 에러가 발생한다.
{% endhint %}

<figure><img src="../.gitbook/assets/스크린샷 2024-01-18 시간 18.31.06.png" alt=""><figcaption></figcaption></figure>

이후 가장 아래 변경사항을 저장한다.



이후, 내 버킷에서 이미지를 클릭후 해당 이미지를 확인하면 에러가 나지않고 이미지를 볼수 있다.



다음은 Next js를 사용해서 이미지를 읽기, 쓰기, 삭제, 수정 등을 해보자.

우선 그전에 AWS IAM에 대해서 알아보자.

{% content-ref url="../aws-iam/" %}
[aws-iam](../aws-iam/)
{% endcontent-ref %}

