---
title: "[Spring Security] 스프링 시큐리티 - 권한 설정"
header:
categories:
  - Java
tags:
  - Spring Security
sidebar:
    nav: temp
toc: true

gallery:
- url: https://lh3.googleusercontent.com/fife/ABSRlIqst6byBcraSFbd4r2L3r61LG1r5VvlLzRtlNpGgHMnQF_Fmjofy6MGmAwumRM_k4vi6rfNjtn9h7Owh2XuynFzgsFay0A8x7aW3OLe-efvu7RRvXDs-b-ifN-NLvdfEf-rAG9B8u45tcQSdFdHe2qZ4jUUFIsJpUspDC1mVR0_7fXxWbQcHQBbnKIv-CiE-A0I77aTz6Ga0RHZgmdI_sYNdGWt23V3yzyp57gRqO2MQLy8Fymi0gnCCE17kqbMPUfN84jR8J7CVU_OTNNgAH4eshYMiE1LpY3ksIXspOKDB8RMi7-kXeJTiBaTP1diLkBjhNd0H40sB643F59Qy3pLpmFuvIIRaBCRnBMDEM6-PasECXCl7eT6RIBevfFWdRDqE81JrosvmkysNBR1EKGPTc38RGs9XJIdXAbSBPt1CjZqF6uY-30DtvxWpT2bfoFT6QOdeRpusv4UO111M3DDjn7FUO-X3fz0qxGzCiGx0-DmkO--bHZ9nG72xKnk8JHWc94qWrbgFEh5VJcaWEw4Jkp5_WAYkNvfPIq9esK18irUq8NwmzasZ2bwEvrxJVYhE00nFXHGZ0E8i3MZU1ril_RkA4gVaeIecaJl4QCIhw2gVGomEHImPRqCxt8me-4XOBZ2PXVMs5I67sYSEuceKyGxvDovo_wZSatEQdt2_ZnH38KU6-1VqyNv94Z1PKgJvfdJrpDALXeMFaDr52FfuA9QreTdA9I=w3030-h1980-ft
  image_path: https://lh3.googleusercontent.com/fife/ABSRlIqst6byBcraSFbd4r2L3r61LG1r5VvlLzRtlNpGgHMnQF_Fmjofy6MGmAwumRM_k4vi6rfNjtn9h7Owh2XuynFzgsFay0A8x7aW3OLe-efvu7RRvXDs-b-ifN-NLvdfEf-rAG9B8u45tcQSdFdHe2qZ4jUUFIsJpUspDC1mVR0_7fXxWbQcHQBbnKIv-CiE-A0I77aTz6Ga0RHZgmdI_sYNdGWt23V3yzyp57gRqO2MQLy8Fymi0gnCCE17kqbMPUfN84jR8J7CVU_OTNNgAH4eshYMiE1LpY3ksIXspOKDB8RMi7-kXeJTiBaTP1diLkBjhNd0H40sB643F59Qy3pLpmFuvIIRaBCRnBMDEM6-PasECXCl7eT6RIBevfFWdRDqE81JrosvmkysNBR1EKGPTc38RGs9XJIdXAbSBPt1CjZqF6uY-30DtvxWpT2bfoFT6QOdeRpusv4UO111M3DDjn7FUO-X3fz0qxGzCiGx0-DmkO--bHZ9nG72xKnk8JHWc94qWrbgFEh5VJcaWEw4Jkp5_WAYkNvfPIq9esK18irUq8NwmzasZ2bwEvrxJVYhE00nFXHGZ0E8i3MZU1ril_RkA4gVaeIecaJl4QCIhw2gVGomEHImPRqCxt8me-4XOBZ2PXVMs5I67sYSEuceKyGxvDovo_wZSatEQdt2_ZnH38KU6-1VqyNv94Z1PKgJvfdJrpDALXeMFaDr52FfuA9QreTdA9I=w3030-h1980-ft
  alt: "스프링 시큐리티 로그인"
  title: "스프링 시큐리티 로그인"
- url: https://lh3.googleusercontent.com/fife/ABSRlIrA5x_b_gKHhPeWu-3ewkxmG5owEUpVmhzkV_6vCx2oBzdjdanaFizHPGG3xDj4LtHryUtI9hV05LKBnOImLUqHyiuI5Ao7xwKLlTzQPyPF_d18t6Ip-2yBdGWSp_GMCbrwV5NpsW2M7txgpr-MuH8DfY5hRsqAur_t2t6G4nwpgOrT4_zBDEI0wJx5VAOAdZSy-zQ9CNHFfEelkybeZDXAEJhtggL9okENuTGM82LR8akOrvhd1fwyMwR5an_f6xL_ZpLZjdk-Sz9bmhiLMqAzLKBeL1oSE-YadoyGexsgXMxlBTvjdTaHTi6gRUYFkZD-j_iy4_vLsyX5FrI43Htd66P2NvcHR2Qnejerusj0rTP0A9ccTiV5e_PtnmE_JFyyH2wukOUi3-dDffQTdQCUiBd2b--x2D4J1WrOVADRlW6M8XOSbw_1xWeCg86o6UmcECzvXEF5TLnfF5px7l_Bg9XoB3fn5hOsgezALd8LYvh6MF1WW9r4RiDPdPwk5kQ8xHulHrJXxPSF4rcRUFxUCFPsHRheOlJ5ljPqInLSXlBaeirFzGgNR9RkeZXxb1cgVWa_woNbMwkxjJ2jQOGr3ExiWw5XljBHxMk-543L7-r8--32q0tGvevWVI5A_SZ1gR1-Q848ojMMN8lJOpJMiZpBMa93T5VeaRvweNFxlJihwSKdDh-vKXeZWYLTIoGbOy19J4Wf7AIPZLppQhtHjjn1S_u3wOE=w2103-h1980-ft
  image_path: https://lh3.googleusercontent.com/fife/ABSRlIrA5x_b_gKHhPeWu-3ewkxmG5owEUpVmhzkV_6vCx2oBzdjdanaFizHPGG3xDj4LtHryUtI9hV05LKBnOImLUqHyiuI5Ao7xwKLlTzQPyPF_d18t6Ip-2yBdGWSp_GMCbrwV5NpsW2M7txgpr-MuH8DfY5hRsqAur_t2t6G4nwpgOrT4_zBDEI0wJx5VAOAdZSy-zQ9CNHFfEelkybeZDXAEJhtggL9okENuTGM82LR8akOrvhd1fwyMwR5an_f6xL_ZpLZjdk-Sz9bmhiLMqAzLKBeL1oSE-YadoyGexsgXMxlBTvjdTaHTi6gRUYFkZD-j_iy4_vLsyX5FrI43Htd66P2NvcHR2Qnejerusj0rTP0A9ccTiV5e_PtnmE_JFyyH2wukOUi3-dDffQTdQCUiBd2b--x2D4J1WrOVADRlW6M8XOSbw_1xWeCg86o6UmcECzvXEF5TLnfF5px7l_Bg9XoB3fn5hOsgezALd8LYvh6MF1WW9r4RiDPdPwk5kQ8xHulHrJXxPSF4rcRUFxUCFPsHRheOlJ5ljPqInLSXlBaeirFzGgNR9RkeZXxb1cgVWa_woNbMwkxjJ2jQOGr3ExiWw5XljBHxMk-543L7-r8--32q0tGvevWVI5A_SZ1gR1-Q848ojMMN8lJOpJMiZpBMa93T5VeaRvweNFxlJihwSKdDh-vKXeZWYLTIoGbOy19J4Wf7AIPZLppQhtHjjn1S_u3wOE=w2103-h1980-ft
  alt: "로그인 성공"
  title: "로그인 성공"  
---

이클립스에서 개인 프로젝트를 해본 후 복습할 필요가 있는 것 같아 시작부터 적용까지 기록을 남기기로 했다.

### pom.xml ( 메이븐 설정 )
```xml

    <!-- https://mvnrepository.com/artifact/org.springframework.security/spring-security-core -->
    <dependency>
        <groupId>org.springframework.security</groupId>
        <artifactId>spring-security-core</artifactId>
        <version>5.2.3.RELEASE</version>
    </dependency>
    <!-- https://mvnrepository.com/artifact/org.springframework.security/spring-security-web -->
    <dependency>
        <groupId>org.springframework.security</groupId>
        <artifactId>spring-security-web</artifactId>
        <version>5.2.3.RELEASE</version>
    </dependency>
    <!-- https://mvnrepository.com/artifact/org.springframework.security/spring-security-config -->
    <dependency>
        <groupId>org.springframework.security</groupId>
        <artifactId>spring-security-config</artifactId>
        <version>5.2.3.RELEASE</version>
    </dependency>
    <!-- https://mvnrepository.com/artifact/org.springframework.security/spring-security-taglibs -->
    <dependency>
        <groupId>org.springframework.security</groupId>
        <artifactId>spring-security-taglibs</artifactId>
        <version>5.2.3.RELEASE</version>
    </dependency>

```
pom.xml에 스프링 시큐리티에 필요한 의존성을 추가해 준다.  
버전 : 5.2.3.RELEASE는 현재 환경에 맞춘 설정이고 ${org.springframework-version}를 사용하여 현재 프레임워크 버전에 맞추어도 된다.

### web.xml 설정
```xml

    <context-param>
        <param-name>contextConfigLocation</param-name>
        <param-value>
            /WEB-INF/applicationContext.xml
            /WEB-INF/spring/security-context.xml    <!-- 추가 -->
        </param-value>
    </context-param>
    
    <!-- 추가 -->
    <filter>
      <filter-name>springSecurityFilterChain</filter-name>
      <filter-class>org.springframework.web.filter.DelegatingFilterProxy</filter-class>
    </filter>
    <filter-mapping>
      <filter-name>springSecurityFilterChain</filter-name>
      <url-pattern>/*</url-pattern>
    </filter-mapping>

```
param-value에 security-context.xml 경로 추가  
스프링 시큐리티 필터 추가  
모든 요청이 필터를 거쳐가기 위해 url-pattern에 /*

### security-context.xml 작성
WEB-INF / security-context.xml 생성  
경로 변경 시 web.xml에 param-value 경로 수정 필요
```xml

    <?xml version="1.0" encoding="UTF-8"?>
    <beans:beans xmlns="http://www.springframework.org/schema/security"
                 xmlns:beans="http://www.springframework.org/schema/beans"
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                 xsi:schemaLocation="http://www.springframework.org/schema/beans
                 http://www.springframework.org/schema/beans/spring-beans.xsd
                 http://www.springframework.org/schema/security
                 http://www.springframework.org/schema/security/spring-security.xsd">
    
        <http auto-config="true" use-expressions="false">
            <intercept-url pattern="/**" access="ROLE_USER" />
        </http>
    
        <authentication-manager>
            <authentication-provider>
                <user-service>
                    <user name="admin" password="{noop}admin" authorities="ROLE_ADMIN"/>
                    <user name="user" password="{noop}user" authorities="ROLE_USER"/>
                </user-service>
            </authentication-provider>
        </authentication-manager>
    
    </beans:beans>

```

{% include gallery id="gallery" layout="half" caption="스프링 시큐리티 로그인 화면(왼쪽) 로그인 성공(오른쪽)" %}