---
title: Requisitos técnicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: En este tema se describe los lenguajes de programación compatibles, método y la visibilidad de COM devuelven requisitos de tipo y obtener información detallada de la extensibilidad de proveedor de Outlook Social Connector (OSC) DLL.
ms.openlocfilehash: 94b57e20957f3d8d779c4d3324ecbb8ccd37f60a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821214"
---
# <a name="technical-requirements"></a>Requisitos técnicos

En este tema se describe los lenguajes de programación compatibles, método y la visibilidad de COM devuelven requisitos de tipo y obtener información detallada de la extensibilidad de proveedor de Outlook Social Connector (OSC) DLL. 
  
## <a name="programming-language-and-com-requirements"></a>Lenguaje de programación y los requisitos de COM

Puede crear un proveedor de OSC mediante lenguajes administrados como Visual C# o Visual Basic o lenguajes no administrados como Visual C++. Puede usar cualquier herramienta que puede crear un componente COM-visible DLL para desarrollar un proveedor de OSC. La decisión de usar un lenguaje administrado o no administrado para desarrollar un proveedor debe tener en cuenta el tamaño de la descarga y las dependencias del paquete de instalación del proveedor.
  
Un proveedor de OSC debe ser visible a través de COM, tal como se define por lo siguiente:
  
- Después de la instalación, se debe registrar un proveedor de OSC mediante el uso de registro de COM automático o regsvr32.
    
- El registro de un proveedor de OSC DLL de COM registra el proveedor en HKCU o HKLM. 
    
- ProgID de un proveedor aparece registrado en `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- Un proveedor de OSC desarrollado en un lenguaje administrado es COM-visible.
    
- Un proveedor de OSC debe agregar valores al registro de Windows que indican que el archivo DLL del proveedor admite apartamento de un único subproceso (STA) y apartamento multiproceso (MTA) modelos de subprocesos. Para obtener más información acerca de los modelos de subprocesos de COM, vea [funcionamiento de OLE Threading modelos y descripciones](http://support.microsoft.com/kb/150777).
    
Métodos de extensibilidad de proveedores OSC deben devolver tipos primitivos como **cadena** o **bool**. Determinadas **cadena** devolver valores deben cumplir con la definición del esquema para la extensibilidad de proveedor OSC. XML sólo se admite como un valor devuelto. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Detalles de la extensibilidad del proveedor OSC DLL

El componente que admite la extensibilidad del proveedor OSC es la extensibilidad del proveedor OSC DLL. Los programadores de terceros pueden generar archivos DLL de proveedor OSC mediante el uso de estas interfaces de extensibilidad. En la siguiente lista muestra los detalles de la extensibilidad del proveedor OSC DLL:
  
- Nombre de archivo del archivo DLL de extensibilidad: socialprovider.dll
    
- Nombre descriptivo del archivo DLL de extensibilidad: extensibilidad de proveedor de Microsoft Outlook Social
    
- Versión principal del archivo DLL de extensibilidad: 15.0
    
- Versión de la biblioteca de tipos de archivo DLL de Extensibiilty: 1.1
    
## <a name="miscellaneous-technical-information"></a>Varias información técnica

No se admite JavaScript Object Notation (JSON) en el modelo de extensibilidad de proveedor OSC.
  
No hay ninguna dependencia en un analizador de XML. El proveedor de OSC puede usar un analizador de XML que se incluye con Office, como Microsoft XML Core Services (MSXML), use las funciones integradas en Microsoft .NET Framework de análisis de XML o usar un analizador XML de otros fabricantes. 
  
## <a name="see-also"></a>Ver también

- [Prácticas recomendadas para desarrollar un proveedor](best-practices-for-developing-a-provider.md)  
- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implementación de un proveedor](deploying-a-provider.md)  
- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

