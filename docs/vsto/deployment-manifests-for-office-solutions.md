---
title: Office 솔루션의 배포 매니페스트
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office applications [Office development in Visual Studio], deployment manifests
- deployment manifests [Office development in Visual Studio]
- manifests [Office development in Visual Studio], deployment
- Office development in Visual Studio, deployment manifests
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 3c96f0d87f5a49add1f0e8cebb61bab9659277e6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62972397"
---
# <a name="deployment-manifests-for-office-solutions"></a>Office 솔루션의 배포 매니페스트
  배포 매니페스트는 Office 솔루션의 배포 설정에 설명 하 고 응용 프로그램의 현재 버전을 식별 하는 XML 파일입니다.

 Visual Studio에서 Office 개발에 사용 하는 [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] 에 정의 된 배포 매니페스트 스키마를 [ClickOnce 배포 매니페스트](../deployment/clickonce-deployment-manifest.md) 참조.

## <a name="remarks"></a>설명
 Office 솔루션에 대 한 배포 매니페스트 파일에는 현재 버전 및 기타 배포 설정을 식별 합니다. 응용 프로그램 매니페스트를 참조 하 고 솔루션 및 솔루션의 모든 파일 내에서 현재 버전을 설명 합니다.

## <a name="file-name-syntax"></a>파일 이름 구문
 배포 매니페스트 파일의 이름으로 끝나야 합니다 *.vsto* 확장 합니다. 표준 이지만 [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] 배포 매니페스트 파일을 처리 하도록 Visual Studio Tools for Office runtime 사용 하도록 설정 하려면 확장명이 달라 집니다.

## <a name="example"></a>예제
 다음 코드 예제는 Visual Studio Tools for Office 솔루션에 대 한 배포 매니페스트를 보여 줍니다.

```xml
<?xml version="1.0" encoding="utf-8"?>
<asmv1:assembly
  xsi:schemaLocation=
    "urn:schemas-microsoft-com:asm.v1 assembly.adaptive.xsd"
  manifestVersion="1.0"
  xmlns:asmv3="urn:schemas-microsoft-com:asm.v3"
  xmlns:dsig="http://www.w3.org/2000/09/xmldsig#"
  xmlns:co.v1="urn:schemas-microsoft-com:clickonce.v1"
  xmlns:co.v2="urn:schemas-microsoft-com:clickonce.v2"
  xmlns="urn:schemas-microsoft-com:asm.v2"
  xmlns:asmv1="urn:schemas-microsoft-com:asm.v1"
  xmlns:asmv2="urn:schemas-microsoft-com:asm.v2"
  xmlns:xrml="urn:mpeg:mpeg21:2003:01-REL-R-NS"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <assemblyIdentity
    name="ContosoOfficeSolutions.vsto"
    version="1.0.0.0"
    publicKeyToken="25d0f3ca94156f1f"
    language="neutral"
    processorArchitecture="msil"
    xmlns="urn:schemas-microsoft-com:asm.v1" />
  <description
    asmv2:publisher="Microsoft"
    asmv2:product="ContosoOfficeSolutions"
    xmlns="urn:schemas-microsoft-com:asm.v1" />
  <deployment install="false" mapFileExtensions="true" />
  <dependency>
    <dependentAssembly
      dependencyType="install"
      codebase="ContosoOfficeSolutions.dll.manifest"
      size="13545">
      <assemblyIdentity
        name="ContosoOfficeSolutions.dll"
        version="1.0.0.0"
        publicKeyToken="25d0f3ca94156f1f"
        language="neutral"
        processorArchitecture="msil"
        type="win32" />
      <hash>
        <dsig:Transforms>
          <dsig:Transform Algorithm=
            "urn:schemas-microsoft-com:HashTransforms.Identity" />
        </dsig:Transforms>
        <dsig:DigestMethod Algorithm=
          "http://www.w3.org/2000/09/xmldsig#sha1" />
        <dsig:DigestValue>PoY</dsig:DigestValue>
      </hash>
    </dependentAssembly>
  </dependency>
  <publisherIdentity name="name" issuerKeyHash="003" />
<Signature
  Id="StrongNameSignature"
  xmlns="http://www.w3.org/2000/09/xmldsig#">
  <SignedInfo>
    <CanonicalizationMethod Algorithm=
      "http://www.w3.org/2001/10/xml-exc-c14n#" />
  <SignatureMethod Algorithm=
    "http://www.w3.org/2000/09/xmldsig#rsa-sha1" />
    <Reference URI="">
      <Transforms>
        <Transform Algorithm=
          "http://www.w3.org/2000/09/xmldsig#enveloped-signature" />
        <Transform Algorithm=
          "http://www.w3.org/2001/10/xml-exc-c14n#" />
      </Transforms>
      <DigestMethod Algorithm=
        "http://www.w3.org/2000/09/xmldsig#sha1" />
      <DigestValue>5oz</DigestValue>
    </Reference>
  </SignedInfo>
  <SignatureValue>nNG</SignatureValue>
  <KeyInfo Id="StrongNameKeyInfo">
    <KeyValue>
      <RSAKeyValue>
        <Modulus>ufI</Modulus>
        <Exponent>AQAB</Exponent>
      </RSAKeyValue>
    </KeyValue>
    <msrel:RelData
      xmlns:msrel=
        "http://schemas.microsoft.com/windows/rel/2005/reldata">
      <r:license
        xmlns:r="urn:mpeg:mpeg21:2003:01-REL-R-NS"
        xmlns:as=
          "http://schemas.microsoft.com/windows/pki/2005/Authenticode">
        <r:grant>
          <as:ManifestInformation
            Hash="099"
            Description=""
            Url="">
            <as:assemblyIdentity
              name="ContosoOfficeSolutions.vsto"
              version="1.0.0.0"
              publicKeyToken="25d0f3ca94156f1f"
              language="neutral"
              processorArchitecture="msil"
              xmlns="urn:schemas-microsoft-com:asm.v1" />
          </as:ManifestInformation>
          <as:SignedBy />
          <as:AuthenticodePublisher>
            <as:X509SubjectName>CN=DDNET\BAAdmin</as:X509SubjectName>
          </as:AuthenticodePublisher>
        </r:grant>
        <r:issuer>
          <Signature
            Id="AuthenticodeSignature"
            xmlns="http://www.w3.org/2000/09/xmldsig#">
            <SignedInfo>
              <CanonicalizationMethod
                Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#" />
              <SignatureMethod
                Algorithm=
                  "http://www.w3.org/2000/09/xmldsig#rsa-sha1" />
              <Reference URI="">
                <Transforms>
                  <Transform Algorithm=
                    "http://www.w3.org/2000/09/xmldsig#enveloped-signature" />
                  <Transform Algorithm=
                    "http://www.w3.org/2001/10/xml-exc-c14n#" />
                </Transforms>
                <DigestMethod
                  Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />
                <DigestValue>iAd</DigestValue>
              </Reference>
            </SignedInfo>
            <SignatureValue>HL9</SignatureValue>
            <KeyInfo>
              <KeyValue>
                <RSAKeyValue>
                  <Modulus>ufI</Modulus>
                  <Exponent>AQAB</Exponent>
                </RSAKeyValue>
              </KeyValue>
              <X509Data>
                <X509Certificate>MII</X509Certificate>
              </X509Data>
            </KeyInfo>
          </Signature>
        </r:issuer>
      </r:license>
    </msrel:RelData>
  </KeyInfo>
</Signature>
</asmv1:assembly>
```

## <a name="see-also"></a>참고자료

- [Office 솔루션에 대 한 응용 프로그램 매니페스트](../vsto/application-manifests-for-office-solutions.md)