---
title: Usar un objeto de la aplicación de confianza proporcionado por Office Developer Tools para Visual Studio
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7b56e59b19f1c9a0ee4c730f14200c3e501f5290
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406116"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a>Usar un objeto de la aplicación de confianza proporcionado por Office Developer Tools para Visual Studio

Si está desarrollando un complemento administrado mediante Office Developer Tools para Visual Studio, use siempre el objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) que proporciona Visual Studio. 

A menos que desee automatizar una nueva instancia de Outlook, no use la palabra clave New para crear una nueva instancia de Outlook, ya que esta instancia del objeto **Application** no es de confianza desde la perspectiva de la Protección del modelo de objetos de Outlook. 

Si el complemento usa un instancia del objeto **Application** que no sea de confianza, en función de la versión de Outlook que esté ejecutando el cliente, el complemento invocará de manera predeterminada la Protección del modelo de objetos de Outlook en varios miembros del modelo de objetos. 

Para obtener más información sobre el comportamiento de la Protección del modelo de objetos, vea [Code Security Changes in Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)) (Cambios en la seguridad de los códigos en Outlook 2007). Tenga en cuenta que, aunque el artículo "Code Security Changes in Outlook 2007" hace referencia a los complementos COM que son de confianza de forma predeterminada, este diseño se aplica a las versiones de Outlook a partir de Outlook 2007, y la confianza se aplica de la misma manera a los complementos administrados. Independiente de que el complemento sea o no administrado, la confianza se basa en el supuesto de que el complemento usa un objeto **Application** de confianza.

