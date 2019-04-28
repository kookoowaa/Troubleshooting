## Problem

- 리눅스 데스크탑 환경에서 

## Resolution

- 슈퍼유저 권한 부여

  ```shel
  sudo usermod -a -G sudo <username>
  ```

- 해당 유저 비밀번호 설정

  ```she
  sudo passwd <username>
  ```

- 해결이 안될 시, `policykit` 권한 조정

  ```
  sudo nano usr/share/polkit-1/actions/org.debian.apt.policy
  
  ## 이하 부분 변경
  <defaults>
  <allow_any>yes</allow_any>
  <allow_inactive>no</allow_inactive>
  <allow_active>yes</allow_active>
  </defaults>
  
  ```

  