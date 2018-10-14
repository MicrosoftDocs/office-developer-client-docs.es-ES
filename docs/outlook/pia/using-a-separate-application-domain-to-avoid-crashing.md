---
title: Usar un dominio de aplicación independiente para evitar el bloqueo
TOCTitle: Using a separate application domain to avoid crashing
ms:assetid: 7fc6d1e5-7032-47a9-826f-6b5d3b43fef9
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb623114(v=office.15)
ms:contentKeyID: 55119786
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b397fa2ad37102e12a3a0cf569e74323391b8e86
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407257"
---
# <a name="using-a-separate-application-domain-to-avoid-crashing"></a>Usar un dominio de aplicación independiente para evitar el bloqueo

Los complementos administrados que implementan la interfaz **IDTExtensibility2** se cargan en el mismo dominio de aplicación predeterminado. Cuando se bloquea un complemento en el dominio de aplicación, puede provocar errores en otros complementos del mismo dominio de aplicación.

Para solucionar este problema, puede crear una corrección de compatibilidad (shim) para el complemento, para que el complemento pueda cargarse en su propio dominio de aplicación. Una corrección de compatibilidad (shim) es una biblioteca de vínculos dinámicos no administrada escrita en C++. Al usar una corrección de compatibilidad (shim), se registra la corrección de compatibilidad en lugar del complemento. Outlook carga la corrección de compatibilidad, y la corrección de compatibilidad carga el complemento para el cual se creó. Debe compilar y registrar una corrección de compatibilidad independiente para cada complemento. Para obtener más información sobre el desarrollo de correcciones de compatibilidad para complementos administrados, consulte [Isolating Office Extensions with the COM Shim Wizard](https://go.microsoft.com/fwlink/?linkid=89109) (Aislar extensiones de Office con el asistente COM Shim).

Otra alternativa para cargar el complemento en otro dominio de aplicación es desarrollar el complemento con Herramientas de desarrollo de Office en Visual Studio 2010, o una versión posterior de Developer Tools para Visual Studio Los complementos desarrollados por estas versiones de Office Developer Tools para Visual Studio no implementan la interfaz IDTExtensibility2, sino que usan la interfaz **IStartup**. Usan un cargador proporcionado por Visual Studio, AddinLoader.dll, que actúa como una corrección de compatibilidad genérica. Outlook busca en el registro los complementos creados con Visual Studio. 

Si Outlook encuentra estos complementos, Outlook inicia AddinLoader.dll, que a su vez inicia Visual Studio Tools para Office Runtime y transmite el manifiesto de aplicación a Visual Studio Tools para Office Runtime. Después, Visual Studio Tools para Office Runtime carga cada complemento en un dominio de aplicación independiente. Para obtener más información sobre cómo Visual Studio carga un complemento, vea [Architecture of Application-Level Add-Ins](https://msdn.microsoft.com/library/bb386298\(v=office.15\)) (Arquitectura de complementos del nivel de la aplicación).

