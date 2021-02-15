---
title: Ejecución de objetos de negocio en servicios de componentes
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23cb90161e5e0728aa652ae5d496216676f781a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309209"
---
# <a name="running-business-objects-in-component-services"></a>Ejecución de objetos de negocio en servicios de componentes

**Se aplica a:** Access 2013, Office 2013

Los objetos de negocio pueden ser archivos ejecutables (.exe) o bibliotecas de vínculo dinámico (.dll). La configuración que se usa para ejecutar el objeto de negocio depende de si el objeto es un archivo .dll o .exe:

- Los objetos de negocio creados como archivos .exe se pueden llamar a través de DCOM. Si estos objetos de negocio se usan a través de Internet Information Services (IIS), estarán sometidos a un proceso adicional de cálculo de referencias de datos que ralentizará la actuación del cliente.

- Los objetos de negocio creados como archivos .dll se pueden utilizar por medio de IIS (y, por tanto, con HTTP). También se pueden utilizar sobre DCOM por medio de Servicios de componentes (o Microsoft Transaction Server, si está utilizando Windows NT). Los archivos DLL de objetos de negocio deberán registrarse en el equipo de servidor IIS para proporcionar accesibilidad a través de IIS. La sección "[Habilitar una biblioteca DLL para que se ejecute en DCOM](enabling-a-dll-to-run-on-dcom.md)" muestra los pasos necesarios para configurar una biblioteca DLL de modo que se ejecute en DCOM.


> [!NOTE]
> Cuando los objetos de negocio del nivel intermedio se implementan como componentes de Servicios de componentes (con **GetObjectContext**, **SetComplete** y **SetAbort),** pueden usar objetos de contexto de Servicios de componentes (o MTS, si usa Windows NT) para mantener su estado en varias llamadas de cliente. Este escenario es posible con DCOM, que normalmente está implementado entre clientes y servidores de confianza (una intranet). 
>
> En este caso, el objeto [RDS.DataSpace](dataspace-object-rds.md) y el método [CreateObject](createobject-method-rds.md) del cliente se reemplazan con el objeto de contexto de transacción y el método **CreateInstance** (proporcionado por la interfaz **ITransactionContext**), implementados por Servicios de componentes.


## <a name="see-also"></a>Consulte también

- [Ejecución de objetos de negocio en servicios de componentes (SQL Server)](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
