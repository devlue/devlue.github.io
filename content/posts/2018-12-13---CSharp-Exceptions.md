---
title: C#/.NET Exception 종류와 설명
date: "2018-12-13T00:00:00.000Z"
template: "post"
draft: false
slug: "csharp-tip"
category: "C#"
tags:
  - "Development"
  - "C#"
  - ".NET"
description: ""
socialImage: "/media/csharp_exception.png"
---

![Image]({{ site.url }}/media/csharp_exception.png)

| Exception Type | Description |
| --- | --- |
| Exception | .NET Framework에서 모든 예외들의 Main 클래스 | 
| AmbiguousMatchException | 클래스를 호출했는데, 어떤 클래스인지 확인할 수 없을 때 발생 |
| ArgumentException | 메서드의 Argument(Parameter)가 유효하지 않을 때 발생 |
| ArgumentNullException | 메서드의 Argument가 허용할 수 없는 null Reference 일 때 발생 |
| ArgumentOutOfRangeException | 메서드의 Argument가 허용할 수 없는 범위 외의 값일 때 발생  |
| AppDomainUnloadedException | 로드되지 않은 어플리케이션 도메인에 접근하려고 할 때 발생 | 
| ArithmeticException | 계산상의 오류가 있을 때 발생 |
| ArrayTypeMismatchException | 두 배열이 동일한 타입의 배열인지 확인한 뒤 같지 않을 때 발생 |
| BadImageFormatException | DLL이나 실행 프로그램의 이미지가 올바르지 않을 때 발생 |
| CannotUnloadAppDomainException | 어플리케이션의 도메인 언로드에 실패할 때 발생 |
| ConfigurationException | 환경설정의 오류가 있을 때 발생 |  
| ContextMarshalException | 마샬링(아래 설명추가)을 하는데 실패할 때 발생 |
| CryptographicExcpetion | 암호화 작업중 오류가 있을 때 발생 |
| DataException | .NET 구성 요소를 사용해서 오류가 있을 때 발생 |
| DivideByZeroException | 0으로 나눗셈을 하려고 할 때 발생 |
| ExecutionEngineException | 실행 엔진 오류가 있을 때 발생 |
| - .NET 4.5부터는 사용하지 않음 | |
| ExternalException | 모든 COM interop 예외 및 SEH 예외에 대한 기본 예외 형식 |
| *대표적인 케이스<br />- Data.Common.DbException<br />- Data.OleDb.OleDbException<br />- Messaging.MessageQueueException<br />- Runtime.InteropServices.COMException<br />- Runtime.InteropServices.SEHException<br />- Web.HttpException<br /> | |
| FileNotFoundException | 찾는 파일이 없을 때 발생 |
| FormatException | Argument로 쓰이는 문자열 서식이 잘못되거나 그 사양에 맞지 않을 때 발생 |
| IndexOutOfRangeException | 배열에서 찾고자 하는 인덱스(순서)가 범위 밖에 있을 때 발생 | 
| InvalidCastException | Type Casting 에 실패할 때 발생 |
| NullReferenceException | 참조하는 Reference가 null일 때 발생 |
| OutOfMemoryException | 메모리 영역을 넘어가는 값이나 Reference를 가져올 때 발생 |
 
 <br />
 
#### * Exception
 ApplicationException / SystemException / IOException 등의 부모 클래스

#### * SystemException
 ArithmeticException / ArgumentException / OutOfMemoryExcpetion / NullReferenceException / IndexOutOfRangeException 등의 부모 클래스

#### * IOException
EndOfStreamException / FileNotFoundException / DirectoryNotFoundException 등의 부모 클래스

#### * ArithmeticException ( 계산상의 오류 )
- DivideByZeroException
- OverflowException

#### * ArgumentException ( Argument 오류 - 파라미터 관련 )
- ArgumentOutOfRangeException
- ArgumentNullException

#### * 마샬링<Marshalling>이란? 
데이터를 전송하기 위한 포맷으로 변환하는 것을 말한다. ( 전송하기 위해 만들었던 포맷을 다시 되돌리는 것은 언마샬링<Unmarshalling>)
