---
title: Proveedores OLE DB (referencia de base de datos de escritorio de Access)
TOCTitle: OLE DB providers
ms:assetid: ef412198-eac5-bf86-73fd-574e67276408
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250215(v=office.15)
ms:contentKeyID: 48548576
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 649f1db283b772a0f6798fae0d56a3a80c59e21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288486"
---
# <a name="ole-db-providers"></a>Proveedores OLE DB


**Se aplica a:** Access 2013, Office 2013

La introducción de la [](introduction-to-ado-programming.md) guía del programador de ADO describe la relación entre ADO y el resto de la arquitectura de Acceso a datos de Microsoft. OLE DB define un conjunto de interfaces COM que proporcionan a las aplicaciones un acceso uniforme a los datos almacenados en diversos orígenes de información. Este enfoque permite que un origen de datos comparta sus datos a través de las interfaces que admiten la funcionalidad de administración de base de datos adecuada al origen de datos. Por diseño, la arquitectura de alto rendimiento de OLE DB se basa en el uso de un modelo de servicios flexible basado en componentes. En vez de tener un número predefinido de capas intermedias entre la aplicación y los datos, OLE DB sólo requiere los componentes estrictamente necesarios para realizar una determinada tarea.

Por ejemplo, suponga que un usuario desea ejecutar una consulta. Considere los escenarios siguientes:

  - Los datos residen en una base de datos relacional para la que existe actualmente un controlador ODBC, pero ningún proveedor OLE DB nativo: la aplicación utiliza ADO para comunicarse con el Proveedor OLE DB para ODBC, que carga después el controlador ODBC apropiado. El controlador pasa la instrucción SQL al sistema de administración de bases de datos, que recupera los datos.

  - Los datos residen en Microsoft SQL Server para el que existe un proveedor OLE DB nativo: la aplicación utiliza ADO para comunicarse directamente con el Proveedor OLE DB para Microsoft SQL Server. No se necesita ningún intermediario.

  - Los datos residen en Microsoft Exchange Server, para el que existe un proveedor OLE DB, pero que no expone ningún motor con el fin de procesar consultas SQL: la aplicación utiliza ADO para comunicarse con el Proveedor OLE DB para Microsoft Exchange y llama a un componente de procesador de consultas OLE DB a fin de procesar las consultas.

  - Los datos residen en el sistema de archivos NTFS de Microsoft en forma de documentos: el acceso a los datos se realiza mediante un proveedor OLE DB nativo en Servicios de Microsoft Index Server, que indizan el contenido y las propiedades de los documentos del sistema de archivos para permitir búsquedas eficientes basadas en el contenido.

En todos los ejemplos anteriores, la aplicación puede consultar los datos. Las necesidades del usuario se satisfacen con un número mínimo de componentes. En cada caso, sólo se utilizan componentes adicionales si es necesario y sólo se llama a los componentes necesarios. Esta carga a petición de los componentes que se pueden compartir y volver a usar contribuye en gran medida al alto rendimiento que se obtiene con OLE DB.

Los proveedores se dividen en dos categorías: aquéllos que proporcionan datos y los que proporcionan servicios. Un [proveedor de datos](data-providers.md) tiene sus propios datos y los expone a la aplicación en forma de tabla. Un [proveedor de servicios](service-providers-and-components.md) encapsula un servicio mediante la generación y el consumo de datos, que contribuye a aumentar las características de las aplicaciones ADO. Además, un proveedor de servicios se puede definir con más detalle como [componente de servicio](service-providers-and-components.md), que debe funcionar conjuntamente con otros componentes o proveedores de servicios.

ADO proporciona una interfaz coherente de nivel superior con los diversos proveedores OLE DB.

Esta sección incluye los siguientes temas:

- [Proveedores de datos](data-providers.md)

- [Proveedores y componentes de servicio](service-providers-and-components.md)
