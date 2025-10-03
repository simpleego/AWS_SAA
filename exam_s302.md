알겠습니다. 정답과 해설이 바로 보이지 않도록 접기 기능(Spoiler)을 사용하여 문제를 다시 출제해 드리겠습니다. 각 문제 아래의 '정답 및 해설 보기'를 클릭하면 내용을 확인할 수 있습니다.

-----

### 📝 AWS SAA-C03: S3 예상 문제

-----

#### **문제 1**

한 회사에서 데이터를 처음 30일 동안은 자주 액세스하고 그 이후에는 거의 액세스하지 않습니다. 이 데이터를 저장하는 데 가장 비용 효율적인 S3 스토리지 클래스는 무엇일까요?

  * A. S3 Standard-IA를 사용하여 30일 후에 객체를 전환하도록 수명 주기 정책을 설정합니다.
  * B. 데이터를 S3 Intelligent-Tiering에 저장합니다.
  * C. 데이터를 S3 Standard에 저장하고 변경하지 않습니다.
  * D. 데이터를 S3 Glacier Deep Archive에 직접 업로드합니다.

<br>
&lt;details&gt;
&lt;summary&gt;&lt;strong&gt;정답 및 해설 보기&lt;/strong&gt;&lt;/summary&gt;
&lt;div&gt;

**정답: B. 데이터를 S3 Intelligent-Tiering에 저장합니다.** ✅

**해설:**
**S3 Intelligent-Tiering**은 액세스 패턴을 자동으로 모니터링하여 객체를 가장 비용 효율적인 스토리지 계층으로 이동시킵니다. 데이터 액세스 패턴이 예측 불가능하거나 변동될 때 수동 개입 없이 비용을 최적화할 수 있어 이 시나리오에 가장 적합합니다.

\</div\>
\</details\>

-----

#### **문제 2**

개발자가 실수로 인한 S3 객체의 삭제나 덮어쓰기를 방지하고 싶어 합니다. 어떤 기능을 활성화해야 할까요?

  * A. S3 객체 잠금(Object Lock)
  * B. 서버 측 암호화(Server-Side Encryption)
  * C. S3 버전 관리(Versioning)
  * D. S3 교차 리전 복제(Cross-Region Replication)

<br>
&lt;details&gt;
&lt;summary&gt;&lt;strong&gt;정답 및 해설 보기&lt;/strong&gt;&lt;/summary&gt;
&lt;div&gt;

**정답: C. S3 버전 관리(Versioning)** ✅

**해설:**
\*\*S3 버전 관리(Versioning)\*\*는 객체의 모든 버전을 보존하여 실수로 삭제하거나 덮어쓴 경우에도 이전 상태로 쉽게 복원할 수 있게 해줍니다. 삭제 시에는 객체가 영구적으로 제거되는 대신 '삭제 마커'가 생성되어 데이터를 보호합니다.

\</div\>
\</details\>

-----

#### **문제 3**

전 세계 여러 지역의 사용자들이 대용량 파일을 S3 버킷으로 빠르고 안전하게 업로드해야 합니다. 어떤 기능을 사용해야 할까요?

  * A. S3 전송 가속화(Transfer Acceleration)
  * B. AWS Direct Connect
  * C. Amazon CloudFront
  * D. S3 교차 리전 복제(Cross-Region Replication)

<br>
&lt;details&gt;
&lt;summary&gt;&lt;strong&gt;정답 및 해설 보기&lt;/strong&gt;&lt;/summary&gt;
&lt;div&gt;

**정답: A. S3 전송 가속화(Transfer Acceleration)** ✅

**해설:**
\*\*S3 전송 가속화(Transfer Acceleration)\*\*는 Amazon CloudFront의 글로벌 엣지 네트워크를 활용하여 사용자와 S3 버킷 간의 데이터 전송 경로를 최적화합니다. 이를 통해 지리적으로 멀리 떨어진 사용자도 빠르고 안정적으로 파일을 업로드할 수 있습니다.

\</div\>
\</details\>

-----

#### **문제 4**

한 조직에서 로그 파일을 90일 후에 아카이브하고 7년 후에 삭제하는 정책을 가지고 있습니다. 이 프로세스를 S3에서 자동화하는 가장 좋은 방법은 무엇일까요?

  * A. S3 수명 주기 정책(Lifecycle policies)
  * B. S3 복제 규칙(Replication rules)
  * C. S3 이벤트 알림(Event Notifications)
  * D. 매일 트리거되는 AWS Lambda 함수 사용

<br>
&lt;details&gt;
&lt;summary&gt;&lt;strong&gt;정답 및 해설 보기&lt;/strong&gt;&lt;/summary&gt;
&lt;div&gt;

**정답: A. S3 수명 주기 정책(Lifecycle policies)** ✅

**해설:**
\*\*S3 수명 주기 정책(Lifecycle policies)\*\*은 객체의 라이프사이클을 관리하기 위한 규칙 기반의 자동화 기능입니다. "객체 생성 후 90일이 지나면 아카이브 스토리지로 이동"하고 "7년 후에는 영구 삭제"하는 것과 같은 규칙을 설정하여 비용 관리와 정책 준수를 손쉽게 자동화할 수 있습니다.

\</div\>
\</details\>

-----

#### **문제 5**

EC2 인스턴스에서 실행되는 애플리케이션에 특정 S3 버킷에 대한 읽기 전용 액세스 권한을 부여하려고 합니다. 장기 자격 증명을 사용하지 않고 가장 안전하게 이 작업을 수행하는 방법은 무엇입니까?

  * A. S3 읽기 액세스 권한을 부여하는 정책으로 IAM 역할을 생성하고 EC2 인스턴스에 연결합니다.
  * B. 액세스 키와 비밀 키를 가진 IAM 사용자를 생성하고 EC2 인스턴스에 저장합니다.
  * C. 버킷 정책을 사용하여 버킷에 대한 익명 액세스를 허용합니다.
  * D. S3 액세스 제어 목록(ACL)을 사용하여 EC2 인스턴스의 IP 주소에 액세스 권한을 부여합니다.

<br>
&lt;details&gt;
&lt;summary&gt;&lt;strong&gt;정답 및 해설 보기&lt;/strong&gt;&lt;/summary&gt;
&lt;div&gt;

**정답: A. S3 읽기 액세스 권한을 부여하는 정책으로 IAM 역할을 생성하고 EC2 인스턴스에 연결합니다.** ✅

**해설:**
AWS 서비스가 다른 서비스 리소스에 접근할 때는 \*\*IAM 역할(Role)\*\*을 사용하는 것이 보안 모범 사례입니다. IAM 역할을 EC2 인스턴스에 연결하면, AWS가 자동으로 임시 보안 자격 증명을 관리하고 교체해 줍니다. 이를 통해 액세스 키와 같은 장기 자격 증명을 코드나 인스턴스 내에 저장할 필요가 없어 보안성이 크게 향상됩니다.

\</div\>
\</details\>
