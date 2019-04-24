---
title: Requisitos técnicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: En este tema se describen los lenguajes de programación admitidos, los requisitos de visibilidad de COM y tipo de valor devuelto de los métodos y los detalles de la DLL de extensibilidad del proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329158"
---
# <a name="technical-requirements"></a>Requisitos técnicos

En este tema se describen los lenguajes de programación admitidos, los requisitos de visibilidad de COM y tipo de valor devuelto de los métodos y los detalles de la DLL de extensibilidad del proveedor de Outlook Social Connector (OSC). 
  
## <a name="programming-language-and-com-requirements"></a>Requisitos de COM y lenguaje de programación

Puede crear un proveedor OSC mediante lenguajes administrados como Visual C# o Visual Basic, o lenguajes no administrados como Visual C++. Puede usar cualquier herramienta que pueda crear un componente DLL visible para COM para desarrollar un proveedor de OSC. La decisión de usar un lenguaje administrado o no administrado para desarrollar un proveedor debe tener en cuenta el tamaño de descarga y las dependencias del paquete de instalación del proveedor.
  
Un proveedor OSC debe ser visible a través de COM, como se define en lo siguiente:
  
- Después de la instalación, un proveedor OSC debe registrarse mediante el registro automático de COM o regsvr32.
    
- El registro COM de una DLL del proveedor de OSC registra el proveedor en HKCU o HKLM. 
    
- El ProgID de un proveedor se registra `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`en.
    
- Un proveedor de OSC desarrollado en un lenguaje administrado es visible para COM.
    
- Un proveedor OSC debe agregar valores al registro de Windows que indiquen que el archivo DLL del proveedor admite modelos de subprocesos de apartamento de un solo subproceso (STA) y de Apartamento multiproceso (MTA). Para obtener más información acerca de los modelos de subprocesos COM, vea deScripciones [and Works of OLE threadIng Models](https://support.microsoft.com/kb/150777).
    
Los métodos de la extensibilidad del proveedor OSC deben devolver tipos primitivos, como **String** o **bool**. Algunos valores devueltos por una **cadena** deben cumplir con la definición de esquema de la extensibilidad del proveedor de OSC. Solo se admite XML como un valor devuelto. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Detalles de la DLL de extensibilidad del proveedor OSC

El componente que admite la extensibilidad del proveedor OSC es la DLL de extensibilidad del proveedor OSC. Los programadores de terceros pueden crear dll del proveedor OSC mediante el uso de estas interfaces de extensibilidad. En la siguiente lista se muestran los detalles de la DLL de extensibilidad del proveedor de OSC:
  
- Nombre del archivo DLL de extensibilidad: socialprovider. dll
    
- Nombre descriptivo de DLL de extensibilidad: extensibilidad del proveedor de Microsoft Outlook social
    
- Versión principal del DLL de extensibilidad: 15,0
    
- Versión de biblioteca de archivos DLL de Extensibiilty: 1,1
    
## <a name="miscellaneous-technical-information"></a>Información técnica diversa

La notación de objetos JavaScript (JSON) no se admite en el modelo de extensibilidad del proveedor OSC.
  
No hay ninguna dependencia en un analizador XML. El proveedor OSC puede usar un analizador XML incluido en Office, como Microsoft XML Core Services (MSXML), usar las funciones de análisis XML integradas en Microsoft .NET Framework o usar un analizador XML de terceros. 
  
## <a name="see-also"></a>Vea también

- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)  
- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implementación de un proveedor](deploying-a-provider.md)  
- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

