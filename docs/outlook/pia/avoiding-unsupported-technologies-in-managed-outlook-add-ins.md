---
title: Evitar tecnologías no admitidas en los complementos administrados de Outlook
TOCTitle: Avoiding unsupported technologies in managed Outlook add-ins
ms:assetid: 365fd319-725f-4c4b-b6e7-575f78ed8bda
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610014(v=office.15)
ms:contentKeyID: 55119789
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99cdfc2447e6bf63078eb87bb9546d8b07ee83e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359062"
---
# <a name="avoiding-unsupported-technologies-in-managed-outlook-add-ins"></a>Evitar tecnologías no admitidas en los complementos administrados de Outlook

Algunas tecnologías anteriores a .NET Framework no se admiten en la programación de código administrado. Estas tecnologías son, entre otras, Objetos de datos de colaboración (CDO), Interfaz de programación de aplicaciones de mensajería (MAPI, a menudo denominada MAPI extendida) y Simple MAPI. Estas tecnologías se diseñaron y desarrollaron con código no administrado, y Microsoft no ofrece empaquetadores administrados oficiales para admitir su uso en las aplicaciones administradas. 

Para obtener más información, vea la sección "Las API que se admiten en el código administrado" en el artículo [KB 266353: Las directrices de compatibilidad para el desarrollo de mensajería de cliente](https://go.microsoft.com/fwlink/?linkid=89209).

Sin embargo, Microsoft Outlook ofrece muchas características de modelos de objetos que permiten lograr lo que anteriormente solo CDO y Extensiones de cliente de Exchange (ECE) podían lograr para los programadores. Si usa CDO en una aplicación de Outlook existente no administrada, y si la falta de compatibilidad para CDO en soluciones administradas ha dificultado la migración de la aplicación al código administrado, entonces puede considerar la posibilidad de actualizar la solución al código administrado usando únicamente el modelo de objetos de Outlook y el ensamblado de interoperabilidad primario (PIA), sin tener que recurrir a CDO. 

Para obtener más información sobre una plataforma de Outlook más completa introducida en Outlook 2007 para disminuir la dependencia de CDO y ECE, vea [Novedades para desarrolladores en Outlook 2007 (Parte 1 de 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).

