---
title: Componentes y proveedores de servicios
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 03447b9977c74484eb7455a75fc2255c33c5e4c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308704"
---
# <a name="service-providers-and-components"></a>Componentes y proveedores de servicios


**Se aplica a:** Access 2013, Office 2013

Los proveedores de servicios son componentes que amplían la funcionalidad de los proveedores de datos mediante la implementación de interfaces extendidas que el almacén de datos no admite de forma nativa.

Microsoft Data Access proporciona una *arquitectura de componentes* que permite a componentes individuales y especializados implementar conjuntos discretos de funciones de base de datos, o "servicios", en almacenes con menos funcionalidades. En vez de obligar a que cada almacén de datos proporcione su propia implementación de la funcionalidad ampliada o forzar a las aplicaciones genéricas a que implementen internamente la funcionalidad de base de datos, los componentes de servicios proporcionan una implementación común que puede ser utilizada por cualquier aplicación al obtener acceso a cualquier almacén de datos. El hecho de que una parte de la funcionalidad la implemente de forma nativa el almacén de datos y la otra mediante componentes genéricos es transparente a la aplicación.

Por ejemplo, un motor de cursor, como el Servicio de cursores de Microsoft para OLE DB, es un componente de servicio que puede consumir datos de un almacén de datos secuencial de sólo avance y generar datos desplazables. Otros proveedores de servicios que suele usar ADO son el Proveedor OLE DB de persistencia de Microsoft (para guardar datos en un archivo), el Servicio de forma de datos de Microsoft para OLE DB (para objetos **Recordset** jerárquicos) y el Proveedor de acceso remoto de Microsoft para OLE DB (para llamar a proveedores de datos en un equipo remoto).

Para obtener más información acerca de proveedores de servicios y datos, vea [Apéndice A: Proveedores](appendix-a-providers.md).

