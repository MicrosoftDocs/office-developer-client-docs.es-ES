---
title: Cambios en Access (referencia de escritorio de la base de datos de Access)
TOCTitle: Changes in Access
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3363d1bc3e9b2157ce8d7855a588b98a819246e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485799"
---
# <a name="changes-in-access"></a>Cambios en Access

**Se aplica a:** Access 2013 | Office 2013

Access no incluye compatibilidad con proyectos de datos de Access (ADP). Access presenta un nuevo tipo de aplicación que permite crear una aplicación de Access basada en web. Al usar este tipo de aplicación, puede crear aplicaciones basadas en web que usen el potencial de SQL Server de forma local o en la nube.

Access presenta un nuevo tipo de aplicación que permite crear una aplicación de Access basada en web. Al usar este tipo de aplicación, puede crear aplicaciones basadas en web que usen el potencial de SQL Server de forma local o en la nube.

En una aplicación de Access de SharePoint Server, al crear una tabla, una consulta o una macro de datos en el cliente de Access en el que crea tablas, vistas o desencadenadores en una base de datos de SQL Server. Al usar el cliente de Access, puede abrir la base de datos en otra aplicación que se conecte a SQL Server. Esto permite compartir los datos o cagarlos desde otros sistemas a la aplicación de Access.

Con Office 365 y Access, puede compilar aplicaciones que lleguen a los usuarios sin tener que preocuparse por los retos de implementación, los problemas de instalación de software o las compatibilidades con sistemas operativos. Compile la aplicación en una ubicación y compártala en Internet con el potencial de SQL Azure y SQL Server.

[SQL Azure](https://msdn.microsoft.com/library/azure/ee336279.aspx), la versión en la nube de SQL Server, no admite características en las que los proyectos de datos de Access (ADP) confíen para funcionar. Para admitir los ADP en SQL Azure, Access necesitaría cambios importantes.

Por estos motivos, Access no admite los ADP. Los ADP han sido una gran herramienta para trabajar con SQL Server en un entorno local, sin embargo, han cambiado muchas cosas desde que se introdujeron en Access 2000. Ahora los usuarios esperan que la base de datos esté disponible desde cualquier lugar.

## <a name="adp-support-and-the-future"></a>Soporte de ADP y el futuro

Los ADP siguen funcionando en versiones anteriores de Access. Puede seguir desarrollando las aplicaciones de ADP y seguiremos dando soporte a las versiones anteriores de Access según el [ciclo de vida de soporte técnico](https://support.microsoft.com/gp/lifeselect) estándar. No actualizaremos versiones antiguas de Access para admitir las nuevas versiones de SQL Server o SQL Azure. Por lo tanto, puede encontrar problemas si usa SQL Server 2012 o versiones posteriores con ADP. Los ADP seguirán admitiendo SQL 2008 R2 y anteriores.

En el futuro, los desarrolladores de ADP pueden considerar varias posibilidades distintas:

- **Convertir a una aplicación de Access** : uso de Access, puede importar las tablas a una nueva aplicación de Access y formularios para la aplicación se crean automáticamente para usted. Puede ampliar la funcionalidad de los formularios base que Access crea y los usuarios pueden usar la aplicación en Internet. Aunque es posible que algunas de las funcionalidades que usa en los ADP no estén disponibles ahora, Microsoft se seguirá centrando en las mejoras de los productos para este tipo de aplicaciones.

- **Convertir a una base de datos de escritorio vinculada** – acceso sigue siendo compatible con la creación de bases de datos de escritorio en el formato de archivo .accdb. Puede convertir la aplicación al formato .accdb, incluidos los formularios e informes existentes, y dejar los datos en SQL Server. Puede vincular a la base de datos de SQL Server mediante las tablas vinculadas y la aplicación seguirá funcionando con los mismos datos.

- **Crear una aplicación híbrida** – si la aplicación es grande y no desea convertir todo al mismo tiempo, puede importar los datos en una aplicación de Access y vincularlo a la base de datos de SQL Server desde una .accdb. Esto permite la migración gradual, lo que agrega formularios y funcionalidades con el tiempo a la aplicación de Access mientras conserva la aplicación de cliente como un archivo .accdb con tablas vinculadas a la base de datos de SQL Server detrás de la aplicación de Access.

- **Actualización para .NET Framework** : la aplicación puede ser compleja suficiente que se considere la posibilidad de migrar a una plataforma de desarrollo profesional, como .NET Framework. SQL Server está diseñado para que sea más fácil usar la infraestructura de base de datos existente que ya ha creado y extender la funcionalidad de la aplicación sin tener que reescribir considerablemente el código.

## <a name="conclusion"></a>Conclusión

Access está diseñado para conectar bases de datos con la nube basándose en tecnologías de SharePoint Server y SQL Server y para trabajar fácilmente con Office 365. Access está diseñado para ayudarle a crear y compartir rápidamente aplicaciones empresariales controladas por datos que ayuden a gestionar el negocio.

## <a name="see-also"></a>Vea también

- [Nuevo en Access para desarrolladores](https://msdn.microsoft.com/library/jj250134\(v=office.15\))
- [Ciclo de vida de soporte técnico de Microsoft](https://support.microsoft.com/lifecycle/)
- [Base de datos SQL de Microsoft Azure](https://msdn.microsoft.com/library/azure/ee336279.aspx)

