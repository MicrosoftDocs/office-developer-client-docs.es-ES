---
title: Relación del PIA de Outlook con el modelo de objetos
TOCTitle: Relating the Outlook PIA with the object model
ms:assetid: 2875c324-cead-4250-b81b-3b7458a9f09e
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb609695(v=office.15)
ms:contentKeyID: 55119779
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cbd5083f3adb8a30f5804cc35e0bc8a08d36b5f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342668"
---
# <a name="relating-the-outlook-pia-with-the-object-model"></a>Relación del PIA de Outlook con el modelo de objetos

El ensamblado de interoperabilidad primario (PIA) de Outlook es un ensamblado de interoperabilidad oficialmente publicado por Outlook que define una interfaz administrada para que los complementos administrados interactúen con el modelo de objetos basado en COM de Outlook. [Introducción a la interoperabilidad entre COM y .NET](introduction-to-interoperability-between-com-and-net.md) describe de forma técnica como un ensamblado de interoperabilidad admite una programación de cliente administrado frente a una biblioteca de tipos basada en COM. Este tema proporciona información general sobre cómo se asignan los objetos y los miembros del modelo de objetos de Outlook basado en COM a las correspondientes interfaces y clases administradas en el PIA.

## <a name="helper-objects"></a>Objetos auxiliares

Cuando se comparan los objetos de la biblioteca de tipos de Outlook que aparecen en el examinador de objetos del Editor de Visual Basic, como se muestra en la figura 1, con los objetos del PIA en el examinador de objetos de Visual Studio, como en la figura 2, puede sorprenderse por la gran cantidad de objetos de ayuda adicionales que existen en el PIA. Es posible que note que algunos objetos, como el objeto **Action**, se asigna a una interfaz, la interfaz [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) interfaz, pero otros objetos, como el objeto **Account**, no siempre se asignan exactamente una interfaz correspondiente en el PIA.

**Figura 1. Explorador que muestra objetos en la biblioteca de tipos de Microsoft Outlook basado en COM**

![Explorador que muestra objetos en la biblioteca de tipos de Microsoft Outlook basado en COM](media/pia-vba-project.gif)

**Figura 2. Explorador que muestra objetos en Outlook**

![Explorador que muestra objetos en Outlook](media/pia-object-browser.jpg)

Entre estas interfaces, muchas de ellas tienen nombres que empiezan con un guion bajo ("\_") seguido de un nombre de objeto. Por ejemplo, el objeto **Account** corresponde a una interfaz pública \_Account y una clase pública Account en el examinador de objetos de Visual Studio. De hecho, aunque no se muestra explícitamente en el examinador de objetos de Visual Studio, el objeto **Account** está asignado a dos interfaces y una clase en el PIA: una interfaz [\_Account](https://msdn.microsoft.com/library/bb609471\(v=office.15\)), una coclase [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) y una clase [AccountClass](https://msdn.microsoft.com/library/bb645768\(v=office.15\)). 

Para obtener más información sobre estas interfaces, coclases y clases, de dónde proceden y cómo se asignan los objetos de la biblioteca de tipos al PIA, vea [Objetos de Outlook PIA](objects-in-the-outlook-pia.md).

## <a name="separate-event-interfaces"></a>Interfaces de eventos independientes

Si examina los objetos que tienen eventos, los eventos en el PIA no están agrupados con otros miembros de propiedad y método del objeto, sino que se agrupan para formar sus propias clases, interfaces y controladores de eventos. 

Para más información sobre cómo se asignan los métodos y propiedades desde la biblioteca de tipos al PIA, vea [Métodos y propiedades del PIA de Outlook](methods-and-properties-in-the-outlook-pia.md). Para más información sobre las clases, delegados e interfaces de eventos, vea [Eventos del PIA de Outlook](events-in-the-outlook-pia.md).

## <a name="hidden-and-deprecated-objects"></a>Objetos ocultos y en desuso

El PIA también contiene enumeraciones, miembros y objetos que han quedado en desuso y, opcionalmente, marcados como ocultos en el modelo de objetos COM. La mayoría de estos objetos, miembros y enumeraciones se muestran en el PIA. Sin embargo, se muestran por la integridad del PIA; ya no deberían ser usados por desarrolladores de soluciones y, por tanto, se documentan mínimamente. Existen algunas excepciones como los objetos **\_DocSiteControl** y **\_RecipientControl**, que están ocultos en la biblioteca de tipos, pero se exponen y documentan como objetos de primera clase en la referencia del PIA. 

Para más información sobre el objeto **\_DocSiteControl**, vea [\_DDocSiteControl](https://msdn.microsoft.com/library/bb609520\(v=office.15\)). Para más información sobre el objeto **\_RecipientControl** objeto, vea [ \_DRecipientControl](https://msdn.microsoft.com/library/bb609501\(v=office.15\)).



