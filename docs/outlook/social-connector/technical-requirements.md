---
title: Requisitos técnicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: En este tema se describen los lenguajes de programación admitidos, los requisitos de tipo de visibilidad COM y de devolución de métodos, y los detalles de la DLL de extensibilidad del proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329158"
---
# <a name="technical-requirements"></a>Requisitos técnicos

En este tema se describen los lenguajes de programación admitidos, los requisitos de tipo de visibilidad COM y de devolución de métodos, y los detalles de la DLL de extensibilidad del proveedor de Outlook Social Connector (OSC). 
  
## <a name="programming-language-and-com-requirements"></a>Requisitos com y lenguaje de programación

Puede crear un proveedor de OSC mediante lenguajes administrados como Visual C# o Visual Basic, o lenguajes no administrados como Visual C++. Puede usar cualquier herramienta que pueda crear un componente DLL visible para COM para desarrollar un proveedor de OSC. La decisión de usar un idioma administrado o no administrado para desarrollar un proveedor debe tener en cuenta el tamaño de descarga y las dependencias del paquete de instalación del proveedor.
  
Un proveedor de OSC debe ser visible para COM tal como se define a continuación:
  
- Después de la instalación, un proveedor de OSC debe registrarse mediante el autoinscripción COM o regsvr32.
    
- El registro COM de un DLL de proveedor de OSC registra el proveedor en HKCU o HKLM. 
    
- ProgID de un proveedor está registrado en  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .
    
- Un proveedor de OSC desarrollado en un idioma administrado es visible para COM.
    
- Un proveedor de OSC debe agregar valores al Registro de Windows que indiquen que la DLL del proveedor admite modelos de subprocesos de apartamento de un solo subproceso (STA) y de multiproceso (MTA). Para obtener más información acerca de los modelos de subproceso COM, vea [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).
    
Los métodos de extensibilidad del proveedor OSC deben devolver tipos primitivos como **cadena** o **bool**. Ciertos **valores devueltos** de cadena deben cumplir con la definición de esquema para la extensibilidad del proveedor de OSC. Solo XML se admite como valor devuelto. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Detalles de la DLL de extensibilidad del proveedor de OSC

El componente que admite la extensibilidad del proveedor de OSC es la DLL de extensibilidad del proveedor de OSC. Los desarrolladores de terceros pueden crear DLL de proveedor de OSC mediante estas interfaces de extensibilidad. En la siguiente lista se muestran los detalles de la DLL de extensibilidad del proveedor de OSC:
  
- Nombre de archivo DLL de extensibilidad: socialprovider.dll
    
- Nombre descriptivo de dll de extensibilidad: Extensibilidad Outlook proveedor social de Microsoft
    
- Versión principal de DLL de extensibilidad: 15.0
    
- Versión de Extensibiilty DLL TypeLib: 1.1
    
## <a name="miscellaneous-technical-information"></a>Información técnica diversa

La notación de objetos de JavaScript (JSON) no se admite en el modelo de extensibilidad del proveedor de OSC.
  
No hay dependencias en un analizador XML. El proveedor de OSC puede usar un analizador XML que se incluye con Office, como Microsoft XML Core Services (MSXML), usar las capacidades de análisis XML integradas en Microsoft .NET Framework o usar un analizador XML de terceros. 
  
## <a name="see-also"></a>Vea también

- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)  
- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implementación de un proveedor](deploying-a-provider.md)  
- [Introducción al desarrollo de un Outlook social connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

