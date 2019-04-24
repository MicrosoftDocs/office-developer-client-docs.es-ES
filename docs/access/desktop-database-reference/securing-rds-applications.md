---
title: Proteger aplicaciones RDS
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a531c01750117ae7abbf87e5ba4cb23daf37851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308781"
---
# <a name="securing-rds-applications"></a>Proteger aplicaciones RDS

**Se aplica a:** Access 2013, Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Aspectos de seguridad en Microsoft Internet Explorer

Con las nuevas mejoras de seguridad agregadas a Microsoft Internet Explorer, algunos objetos ADO y RDS están restringidos a ejecutarse solo en un entorno de modo "seguro". Esto requiere tener en cuenta estos aspectos, incluidos las diferentes zonas, niveles de seguridad, comportamiento restrictivo, operaciones no seguras y configuraciones de seguridad personalizadas.

Para obtener más información acerca de estos aspectos, vea "ADO and RDS Security Issues in Microsoft Internet Explorer" (en inglés) en los artículos técnicos sobre Objetos de datos ActiveX (ADO).

## <a name="security-and-your-web-server"></a>Seguridad y el servidor Web

Si usa el objeto [RDSServer. DataFactory](datafactory-object-rdsserver.md) en su servidor Web de Internet, recuerde que al hacerlo se crea un riesgo potencial para la seguridad. Los usuarios externos que obtienen un nombre de origen de datos (DSN) válido, un identificador de usuario y la información de contraseña podrían escribir páginas para enviar cualquier consulta a ese origen de datos. Si desea un acceso más restringido a un origen de datos, una opción consiste en eliminar el objeto **RDSServer.DataFactory** (msadcf.dll) y, en su lugar, usar objetos de negocio personalizados con consultas codificadas de forma rígida.

Para obtener más información sobre las implicaciones de seguridad del uso del objeto RDSServer. DataFactory, vea el boletín de seguridad de Microsoft MS99-025 en el [sitio web de seguridad de Microsoft](https://www.microsoft.com/en-us/security/default.aspx).

## <a name="client-impersonation-and-security"></a>Suplantación de clientes y seguridad

Si la propiedad de **autenticación de contraseña** del servidor Web de IIS está establecida en autenticación de desafío/respuesta de Windows NT (para windows NT 4,0) o en autenticación de Windows integrada (para Windows 2000), los objetos de negocio se invocan en el del cliente. contexto de seguridad. Esto es una característica nueva en RDS 1.5 que permite la suplantación del cliente a través de HTTP. Cuando se trabaja en este modo, el inicio de sesión en el servidor Web (IIS) no es anónimo, sino que usa el identificador de usuario y la contraseña bajo el que se ejecuta el equipo cliente. Si los DSN de ODBC están configurados para usar una conexión de confianza, entonces el acceso a bases de datos, tales como SQL Server, también se produce en el contexto de seguridad del cliente. Esto solo funciona si la base de datos se encuentra en el mismo equipo que el IIS (las credenciales del cliente no se pueden transferir a otro equipo).

Por ejemplo, un cliente, Jesús Escolar, con el identificador de usuario = "JesúsE" y la contraseña = "secreto" ha iniciado una sesión en un equipo cliente. Este cliente ejecuta una aplicación basada en explorador que necesita acceso al objeto **RDSServer.DataFactory** para crear un [Recordset](recordset-object-ado.md) ejecutando una consulta SQL sobre el equipo "MiServidor" que ejecuta IIS. MiServidor, un sistema que ejecuta Windows NT Server 4.0, está configurado para usar autenticación de desafío/respuesta de Windows NT, su DSN de ODBC tiene seleccionado "Usar conexión de confianza", y el servidor también contiene el origen de datos de SQL Server. Cuando se recibe una solicitud en el servidor Web, se le pide al cliente el identificador de usuario y la contraseña. Por lo tanto, la solicitud se registra en mi servidor como procedente de "Jesúse"/"secreto" en\_lugar de IUSERr (que es el valor predeterminado cuando la autenticación de contraseña anónima está activada). Análogamente, al iniciar sesión en el servidor SQL Server, también se usa "JesúsE"/"secreto".

En consecuencia, el modo de autenticación desafío/respuesta de Windows NT para IIS permite que se creen páginas HTML sin que se pida explícitamente al usuario la información de identificador y contraseña necesaria para iniciar una sesión en la base de datos. Si se utilizara el método de autenticación básica de IIS, también se requeriría esto.

## <a name="password-authentication"></a>Autenticación de contraseña

RDS se puede comunicar con un servidor Web de IIS que se ejecuta en cualquiera de los tres modos de autenticación de contraseña: anónimo, básico o desafío/respuesta de NT (llamada autenticación integrada de Windows en Windows 2000). Esta configuración define el modo en que un servidor Web controla el acceso a él, por ejemplo, exigir que un equipo cliente tenga privilegios de acceso explícito en el servidor Web de NT.

