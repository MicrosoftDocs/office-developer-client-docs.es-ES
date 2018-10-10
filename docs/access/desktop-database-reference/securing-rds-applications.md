---
title: Proteger aplicaciones RDS
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16dd0fd983d6e04f01c7d848a8d45f82b0f1c85a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483799"
---
# <a name="securing-rds-applications"></a><span data-ttu-id="b67ed-102">Proteger aplicaciones RDS</span><span class="sxs-lookup"><span data-stu-id="b67ed-102">Securing RDS Applications</span></span>

<span data-ttu-id="b67ed-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b67ed-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="microsoft-internet-explorer-security-issues"></a><span data-ttu-id="b67ed-104">Aspectos de seguridad en Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="b67ed-104">Microsoft Internet Explorer Security Issues</span></span>

<span data-ttu-id="b67ed-p101">Con las nuevas mejoras de seguridad incluidas en Microsoft® Internet Explorer, algunos objetos ADO y RDS están restringidos para ejecutarse sólo en un entorno de modo "seguro". Esto requiere tener en cuenta estos aspectos, incluidos las diferentes zonas, niveles de seguridad, comportamiento restrictivo, operaciones no seguras y configuraciones de seguridad personalizadas.</span><span class="sxs-lookup"><span data-stu-id="b67ed-p101">With new security enhancements added to Microsoft® Internet Explorer, some ADO and RDS objects are restricted to running only in a "safe" mode environment. This requires that you are aware of these issues, including different zones, security levels, restrictive behavior, unsafe operations, and customized security settings.</span></span>

<span data-ttu-id="b67ed-107">Para obtener más información acerca de estos aspectos, vea "ADO and RDS Security Issues in Microsoft Internet Explorer" (en inglés) en los artículos técnicos sobre Objetos de datos ActiveX (ADO).</span><span class="sxs-lookup"><span data-stu-id="b67ed-107">For more information about these issues, see ADO and RDS Security Issues in Microsoft Internet Explorer under ActiveX Data Objects (ADO) Technical Articles.</span></span>

## <a name="security-and-your-web-server"></a><span data-ttu-id="b67ed-108">Seguridad y el servidor Web</span><span class="sxs-lookup"><span data-stu-id="b67ed-108">Security and Your Web Server</span></span>

<span data-ttu-id="b67ed-p102">Si usa el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) en un servidor web de Internet, recuerde que el hacerlo crea un riesgo potencial para la seguridad. Los usuarios externos que obtienen un nombre de origen de datos (DSN) válido, un identificador de usuario y la información de contraseña podrían escribir páginas para enviar cualquier consulta a ese origen de datos. Si desea un acceso más restringido a un origen de datos, una opción consiste en eliminar el objeto **RDSServer.DataFactory** (msadcf.dll) y, en su lugar, usar objetos de negocio personalizados con consultas codificadas de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="b67ed-p102">If you use the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object on your Internet Web server, remember that doing so creates a potential security risk. External users who obtain valid data source name (DSN), user ID, and password information could write pages to send any query to that data source. If you want more restricted access to a data source, one option is to unregister and delete the **RDSServer.DataFactory** object (msadcf.dll), and instead use custom business objects with hard-coded queries.</span></span>

<span data-ttu-id="b67ed-112">Para obtener más información acerca de las implicaciones de seguridad de utilizar el objeto RDSServer.DataFactory, vea el boletín de seguridad de Microsoft MS99-025 en el [sitio Web de seguridad de Microsoft](https://www.microsoft.com/en-us/security/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="b67ed-112">For more information about the security implications of using the RDSServer.DataFactory object, see the Microsoft Security Bulletin MS99-025 on the [Microsoft Security website](https://www.microsoft.com/en-us/security/default.aspx).</span></span>

## <a name="client-impersonation-and-security"></a><span data-ttu-id="b67ed-113">Suplantación de clientes y seguridad</span><span class="sxs-lookup"><span data-stu-id="b67ed-113">Client Impersonation and Security</span></span>

<span data-ttu-id="b67ed-p103">Si la propiedad de **autenticación de contraseña** del servidor web de IIS está establecida como autenticación de desafío/respuesta de Windows NT (para Windows NT 4.0) o como autenticación integrada de Windows (para Windows 2000), entonces la llamada a los objetos de negocio se realiza en el contexto de seguridad del cliente. Esto es una característica nueva en RDS 1.5 que permite la suplantación del cliente a través de HTTP. Cuando se trabaja en este modo, el inicio de sesión en el servidor web (IIS) no es anónimo, sino que usa el identificador de usuario y la contraseña del equipo cliente. Si los DSN de ODBC están configurados para usar una conexión de confianza, entonces el acceso a bases de datos, tales como SQL Server, también se produce en el contexto de seguridad del cliente. Esto solo funciona si la base de datos se encuentra en el mismo equipo que el IIS (las credenciales del cliente no se pueden transferir a otro equipo).</span><span class="sxs-lookup"><span data-stu-id="b67ed-p103">If the **Password Authentication** property for your IIS Web server is set to Windows NT Challenge/Response authentication (for Windows NT 4.0) or to Integrated Windows authentication (for Windows 2000), then business objects are invoked under the client's security context. This is a new feature in RDS 1.5 that allows Client Impersonation over HTTP. When working in this mode, the logon to the Web server (IIS) is not anonymous but uses the user ID and password that the client computer is running under. If the ODBC DSNs are set up to use Trusted Connection, then access to databases, such as SQL Server, also happens under the client's security context. But this only works if the database is on the same computer as the IIS; the client credentials cannot be carried over to yet another computer.</span></span>

<span data-ttu-id="b67ed-119">Por ejemplo, un cliente, Jesús Escolar, con el identificador de usuario = "JesúsE" y la contraseña = "secreto" ha iniciado una sesión en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="b67ed-119">For example, a client, John Doe, with userid="JohnD" and password="secret" is logged on to a client computer.</span></span> <span data-ttu-id="b67ed-120">Este cliente ejecuta una aplicación basada en explorador que necesita acceso al objeto **RDSServer.DataFactory** para crear un [Recordset](recordset-object-ado.md) ejecutando una consulta SQL sobre el equipo "MiServidor" que ejecuta IIS.</span><span class="sxs-lookup"><span data-stu-id="b67ed-120">He runs a browser-based application that needs to access the **RDSServer.DataFactory** object to create a [Recordset](recordset-object-ado.md) by executing an SQL query on the "MyServer" computer running IIS.</span></span> <span data-ttu-id="b67ed-121">MiServidor, un sistema que ejecuta Windows NT Server 4.0, está configurado para usar autenticación de desafío/respuesta de Windows NT, su DSN de ODBC tiene seleccionado "Usar conexión de confianza", y el servidor también contiene el origen de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b67ed-121">MyServer, a system running Windows NT Server 4.0, is set up to use Windows NT Challenge/Response authentication, its ODBC DSN has "Use Trusted Connection" selected, and the server also contains the SQL Server data source.</span></span> <span data-ttu-id="b67ed-122">Cuando se recibe una solicitud en el servidor web, este solicita al cliente el identificador de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="b67ed-122">When a request is received on the Web server, it asks the client for the user ID and password.</span></span> <span data-ttu-id="b67ed-123">Por lo tanto, la solicitud se registra en MiServidor como procedente de "JesúsE" / "Secret" en lugar de IUSER\_MyServer (que es el valor predeterminado cuando la autenticación de contraseña anónima está activado).</span><span class="sxs-lookup"><span data-stu-id="b67ed-123">Thus, the request is logged on MyServer as coming from "JohnD"/"Secret" instead of IUSER\_MyServer (which is the default when Anonymous Password Authentication is on).</span></span> <span data-ttu-id="b67ed-124">Análogamente, al iniciar sesión en el servidor SQL Server, también se usa "JesúsE"/"secreto".</span><span class="sxs-lookup"><span data-stu-id="b67ed-124">Similarly, when logging on to SQL Server, "JohnD"/"Secret" is used.</span></span>

<span data-ttu-id="b67ed-p105">En consecuencia, el modo de autenticación desafío/respuesta de Windows NT para IIS permite que se creen páginas HTML sin que se pida explícitamente al usuario la información de identificador y contraseña necesaria para iniciar una sesión en la base de datos. Si se utilizara el método de autenticación básica de IIS, también se requeriría esto.</span><span class="sxs-lookup"><span data-stu-id="b67ed-p105">Consequently, the IIS Windows NT Challenge/Response authentication mode allows HTML pages to be created without the user being explicitly prompted for the user ID and password information needed to log on to the database. If the IIS Basic Authentication were being used, then this also would be required.</span></span>

## <a name="password-authentication"></a><span data-ttu-id="b67ed-127">Autenticación de contraseña</span><span class="sxs-lookup"><span data-stu-id="b67ed-127">Password Authentication</span></span>

<span data-ttu-id="b67ed-p106">RDS se puede comunicar con un servidor Web de IIS que se ejecuta en los cualquiera de los tres modos de autenticación de contraseña: anónimo, básico o desafío/respuesta de Windows NT (en Windows 2000, se denomina autenticación de Windows integrada). Estas opciones definen cómo un servidor Web controla el acceso a él (por ejemplo, requerir que un equipo cliente tenga privilegios de acceso explícitos en el servidor Web de NT).</span><span class="sxs-lookup"><span data-stu-id="b67ed-p106">RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response authentication (called Integrated Windows authentication in Windows 2000). These settings define how a Web server controls access through it, such as requiring that a client computer have explicit access privileges on the NT Web server.</span></span>
