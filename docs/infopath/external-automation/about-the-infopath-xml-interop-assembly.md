---
title: Acerca del ensamblado de interoperabilidad XML de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- interoperabilidad de MSXML [infopath 2007], InfoPath 2007, ensamblado de interoperabilidad primario de XML, el ensamblado de interoperabilidad XML de InfoPath
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: El ensamblado de interoperabilidad XML de InfoPath se proporciona para permitir la compatibilidad para la interoperabilidad entre código administrado y el servidor COM expuestos por Microsoft XML Core Services (MSXML) desde aplicaciones externas que automatizan InfoPath.
ms.openlocfilehash: 8d3fb1c1de141fe23c655e82b77d83a8e2b11abd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815745"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>Acerca del ensamblado de interoperabilidad XML de InfoPath

El ensamblado de interoperabilidad XML de InfoPath se proporciona para permitir la compatibilidad para la interoperabilidad entre código administrado y el servidor COM expuestos por Microsoft XML Core Services (MSXML) desde aplicaciones externas que automatizan InfoPath.

La opción de **Compatibilidad con programación de .NET** en el programa de instalación de InfoPath instala a los ensamblados de interoperabilidad tres. Los ensamblados de interoperabilidad son ensamblados .NET que actúan como puente entre el código administrado y no administrado, asignando miembros de objetos COM a los miembros administrados .NET equivalentes. Uno de los ensamblados, Microsoft.Office.Interop.InfoPath.Xml.dll, proporciona a los miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) , que se usa para trabajar con los miembros expuestos por el servidor COM de Microsoft XML Core Services (MSXML) desde aplicaciones externas que automatizar InfoPath con código administrado. 
  
> [!NOTE]
> Las referencias a los ensamblados de interoperabilidad Microsoft.Office.Interop.InfoPath.dll y Microsoft.Office.Interop.InfoPath.Xml.dll son necesarios para los proyectos de automatización externa de InfoPath se deben establecer manualmente. Para obtener más información sobre la automatización externa, vea [escenarios de automatización externo y ejemplos](external-automation-scenarios-and-examples.md). 
  
## <a name="see-also"></a>Vea también

- [Trabajar con MSXML y System.Xml con el modelo de objetos de InfoPath 2003](http://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

