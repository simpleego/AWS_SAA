# AWS EC2 인스턴스를 **생성**, **중지**, **종료**하는 명령어
> AWS CLI를 통해 수행할 수 있습니다. 

---

### ✅ 1. EC2 인스턴스 생성 (예: Amazon Linux 2 AMI)
```bash
aws ec2 run-instances \
  --image-id ami-xxxxxxxxxxxxxxxxx \
  --count 1 \
  --instance-type t2.micro \
  --key-name MyKeyPair \
  --security-groups MySecurityGroup
```
- `--image-id`: 사용할 AMI ID
- `--count`: 생성할 인스턴스 수
- `--instance-type`: 인스턴스 타입
- `--key-name`: SSH 접속용 키페어 이름
- `--security-groups`: 보안 그룹 이름

---

### 🛑 2. EC2 인스턴스 중지 (Stop)
```bash
aws ec2 stop-instances --instance-ids i-xxxxxxxxxxxxxxxxx
```
- 인스턴스는 **중지 상태**가 되며, EBS는 유지됩니다.

---

### ❌ 3. EC2 인스턴스 종료 (Terminate)
```bash
aws ec2 terminate-instances --instance-ids i-xxxxxxxxxxxxxxxxx
```
- 인스턴스는 **완전히 삭제**되며, 연결된 EBS도 삭제될 수 있습니다 (삭제 설정에 따라 다름).

---

### 🔍 인스턴스 목록 확인
```bash
aws ec2 describe-instances
```

---

필요하신 작업에 따라 위 명령어를 수정해 사용하시면 됩니다. 혹시 특정 상황에 맞는 예시나 스크립트가 필요하신가요? 예를 들어, 자동화 스크립트나 특정 리전 설정 등도 도와드릴 수 있어요.
