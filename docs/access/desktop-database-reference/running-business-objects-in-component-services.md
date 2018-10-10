---
title: Ejecutar objetos de negocio en servicios de componentes
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41424fd62e915ecb2d54fdb49c939b788f458804
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484540"
---
# <a name="running-business-objects-in-component-services"></a>Ejecutar objetos de negocio en servicios de componentes


**Se aplica a**: Access 2013 | Office 2013

Los objetos de negocio pueden ser archivos ejecutables (.exe) o bibliotecas de vínculo dinámico (.dll). La configuración que se usa para ejecutar el objeto de negocio depende de si el objeto es un archivo .dll o .exe:

  - Los objetos de negocio creados como archivos .exe se pueden llamar a través de DCOM. Si estos objetos de negocio se usan a través de Internet Information Services (IIS), estarán sometidos a un proceso adicional de cálculo de referencias de datos que ralentizará la actuación del cliente.

  - Los objetos de negocio creados como archivos .dll se pueden utilizar por medio de IIS (y, por tanto, con HTTP). También se pueden utilizar sobre DCOM por medio de Servicios de componentes (o Microsoft Transaction Server, si está utilizando Windows NT). Los archivos DLL de objetos de negocio deberán registrarse en el equipo de servidor IIS para proporcionar accesibilidad a través de IIS. La sección "[Habilitar una biblioteca DLL para que se ejecute en DCOM](enabling-a-dll-to-run-on-dcom.md)" muestra los pasos necesarios para configurar una biblioteca DLL de modo que se ejecute en DCOM.


> [!NOTE]
> <P>Cuando los objetos de negocios en el nivel intermedio se implementan como componentes de servicios de componentes (mediante <STRONG>GetObjectContext</STRONG>, <STRONG>SetComplete</STRONG>y <STRONG>SetAbort</STRONG>), pueden usar servicios de componentes (o MTS, si está utilizando Windows NT) para los objetos de contexto mantener su estado entre diferentes llamadas de cliente. Este escenario es posible con DCOM, que normalmente está implementado entre clientes y servidores de confianza (una intranet). En este caso, el objeto <A href="dataspace-object-rds.md">RDS.DataSpace</A> y el método <A href="createobject-method-rds.md">CreateObject</A> del cliente se reemplazan con el objeto de contexto de transacción y el método <STRONG>CreateInstance</STRONG> (proporcionado por la interfaz <STRONG>ITransactionContext</STRONG> ), implementados por Servicios de componentes.</P>


