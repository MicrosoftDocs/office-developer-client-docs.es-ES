---
title: Cambios en Access (referencia de la base de datos de escritorio de Access)
TOCTitle: Changes in Access
description: Access no incluye compatibilidad con proyectos de datos de Access (ADP). Access presenta un nuevo tipo de aplicación que permite crear una aplicación de Access basada en web.
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: de2ff21598639b445f5ff84240b115704b484209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296503"
---
# <a name="changes-in-access"></a>Cambios en Access

**Se aplica a:** Access 2013, Office 2013

Access no incluye compatibilidad con proyectos de datos de Access (ADP). Access presenta un nuevo tipo de aplicación que permite crear una aplicación de Access basada en web. Al usar este tipo de aplicación, puede crear aplicaciones basadas en web que usen el potencial de SQL Server de forma local o en la nube.

En una aplicación de Access de SharePoint Server, al crear una tabla, una consulta o una macro de datos en el cliente de Access en el que crea tablas, vistas o desencadenadores en una base de datos de SQL Server. Al usar el cliente de Access, puede abrir la base de datos en otra aplicación que se conecte a SQL Server. Esto permite compartir los datos o cargarlos desde otros sistemas a la aplicación de Access.

Con Office 365 y Access, puede compilar aplicaciones que lleguen a los usuarios sin tener que preocuparse por los retos de implementación, los problemas de instalación de software o las compatibilidades con sistemas operativos. Compile la aplicación en una ubicación y compártala en Internet con el potencial de SQL Azure y SQL Server.

[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview), la versión en la nube de SQL Server, no admite características en las que los proyectos de datos de Access (ADP) confíen para funcionar. Para admitir los ADP en SQL Azure, Access necesitaría cambios importantes.

Por estos motivos, Access no admite ADP. Los ADP han sido una gran herramienta para trabajar con SQL Server en un entorno local, sin embargo, han cambiado muchas cosas desde que se introdujeron en Access 2000. Ahora los usuarios esperan que la base de datos esté disponible desde cualquier lugar.

## <a name="adp-support-and-the-future"></a>Soporte de ADP y el futuro

Los ADP siguen funcionando en versiones anteriores de Access. Puede seguir desarrollando las aplicaciones de ADP y seguiremos dando soporte a las versiones anteriores de Access según el [ciclo de vida de soporte técnico](https://support.microsoft.com/lifecycle/search) estándar. No actualizaremos versiones antiguas de Access para admitir las nuevas versiones de SQL Server o SQL Azure. Por lo tanto, puede encontrar problemas si usa SQL Server 2012 o versiones posteriores con ADP. Los ADP seguirán admitiendo SQL 2008 R2 y anteriores.

En el futuro, los desarrolladores de ADP pueden considerar varias posibilidades distintas:

- **Convertir a una aplicación de Access**: con Access, puede importar las tablas a una nueva aplicación de Access y los formularios de la aplicación se crearán automáticamente. Puede ampliar la funcionalidad de los formularios base que Access crea y los usuarios pueden usar la aplicación en Internet. Aunque es posible que algunas de las funcionalidades que usa en los ADP no estén disponibles ahora, Microsoft se seguirá centrando en las mejoras de los productos para este tipo de aplicaciones.

- **Convertir a una base de datos de escritorio vinculada**: Access sigue admitiendo la creación de bases de datos de escritorio con el formato de archivo .accdb. Puede convertir la aplicación al formato .accdb, incluidos los formularios e informes existentes, y dejar los datos en SQL Server. Puede vincular a la base de datos de SQL Server mediante las tablas vinculadas y la aplicación seguirá funcionando con los mismos datos.

- **Crear una aplicación híbrida**: si la aplicación es grande y no quiere convertirlo todo a la vez, puede importar los datos a una aplicación de Access y vincular a la base de datos de SQL Server desde un archivo .accdb. Esto permite la migración gradual, lo que agrega formularios y funcionalidades con el tiempo a la aplicación de Access mientras conserva la aplicación de cliente como un archivo .accdb con tablas vinculadas a la base de datos de SQL Server detrás de la aplicación de Access.

- **Actualizar a .NET Framework**: la aplicación puede ser lo suficientemente compleja como para considerar moverla a una plataforma de desarrollo profesional como .NET Framework. SQL Server está diseñado para facilitar el uso de la infraestructura de base de datos existente y ampliar la funcionalidad de la aplicación sin tener que reescribir significativamente el código.

## <a name="conclusion"></a>Conclusión

Access está diseñado para conectar bases de datos con la nube basándose en tecnologías de SharePoint Server y SQL Server y para trabajar fácilmente con Office 365. Access está diseñado para ayudarle a crear y compartir rápidamente aplicaciones empresariales controladas por datos que ayuden a gestionar el negocio.

## <a name="see-also"></a>Vea también

- [Novedades en Access 2013 para desarrolladores](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)


