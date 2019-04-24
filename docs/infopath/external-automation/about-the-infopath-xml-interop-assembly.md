---
title: Información sobre el ensamblado de interoperabilidad XML de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- interoperabilidad de MSXML [InfoPath 2007], InfoPath 2007, ensamblado de interoperabilidad primario de XML, ensamblado de interoperabilidad XML de InfoPath
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: El ensamblado de interoperabilidad XML de InfoPath se proporciona para permitir la compatibilidad con la interoperabilidad entre el código administrado y el servidor COM expuesto por Microsoft XML Core Services (MSXML) desde aplicaciones externas que automatizan InfoPath.
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303783"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>Información sobre el ensamblado de interoperabilidad XML de InfoPath

El ensamblado de interoperabilidad XML de InfoPath se proporciona para permitir la compatibilidad con la interoperabilidad entre el código administrado y el servidor COM expuesto por Microsoft XML Core Services (MSXML) desde aplicaciones externas que automatizan InfoPath.

La opción **compatibilidad con programación de .net** del programa de instalación de InfoPath instala tres ensamblados de interoperabilidad. Los ensamblados de interoperabilidad son ensamblados .NET que actúan como puente entre el código administrado y no administrado, asignando miembros de objetos COM a los miembros administrados .NET equivalentes. Uno de estos ensamblados, Microsoft. Office. Interop. InfoPath. Xml. dll, proporciona los miembros del espacio de nombres [Microsoft. Office. Interop. InfoPath. XML](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) , que se usa para trabajar con miembros expuestos por el servidor com para Microsoft XML Core Services (MSXML) de aplicaciones externas que automatizan InfoPath mediante código administrado. 
  
> [!NOTE]
> Las referencias a los ensamblados de interoperabilidad Microsoft. Office. Interop. InfoPath. dll y Microsoft. Office. Interop. InfoPath. Xml. dll que se requieren para los proyectos de automatización externa de InfoPath deben establecerse manualmente. Para obtener más información sobre la automatización externa, vea [ejemplos y escenarios de automatización externa](external-automation-scenarios-and-examples.md). 
  
## <a name="see-also"></a>Vea también

- [Trabajar con MSXML y System.Xml con el modelo de objetos de InfoPath 2003](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

