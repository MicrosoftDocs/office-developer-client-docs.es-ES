---
title: Tipos de cursores (referencia de base de datos de escritorio de Access)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6493d746f43ac8d923e5b1b9d6dcd3de44b411ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314031"
---
# <a name="types-of-cursors"></a>Tipos de cursores


**Se aplica a:** Access 2013, Office 2013

Como regla general, una aplicación debería utilizar el cursor más sencillo que proporcione el acceso a datos requerido. Cada característica de cursor adicional más allá de lo básico (sólo avance, sólo lectura, estático, con desplazamiento, sin búfer) supone un costo en memoria de cliente, carga de red o rendimiento. En muchos casos, las opciones predeterminadas de cursor generan un cursor más complejo que el que realmente necesita la aplicación.

La elección del tipo de cursor depende de cómo utiliza la aplicación el conjunto de resultados y también de diversas consideraciones de diseño, como el tamaño del conjunto de resultados, el porcentaje de datos con probabilidad de ser utilizados, la susceptibilidad a cambios de datos, y requisitos de rendimiento de la aplicación.

En el caso más básico, la elección del cursor depende de si se necesita cambiar los datos o simplemente verlos:

  - Si sólo necesita desplazarse por un conjunto de resultados, pero sin cambiar los datos, utilice un cursor [de sólo avance](forward-only-cursors.md) o [estático](static-cursors.md).

  - Si tiene un conjunto de resultados grande y sólo necesita seleccionar algunas filas, utilice un cursor con [conjunto de claves](keyset-cursors.md).

  - Si desea sincronizar un conjunto de resultados con incorporaciones, cambios y eliminaciones recientes de todos los usuarios simultáneos, utilice un cursor [dinámico](dynamic-cursors.md).

Aunque cada tipo de cursor parece distinto, tenga en cuenta que estos tipos de cursor no varían mucho más que en el resultado de características y opciones superpuestas.

