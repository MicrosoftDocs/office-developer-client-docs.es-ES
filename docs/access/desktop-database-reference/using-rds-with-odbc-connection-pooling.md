---
title: Utilizar RDS con agrupamiento de conexiones ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87d380fdc52cdee2aa834fd6e78ff1b761a0e93a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312120"
---
# <a name="using-rds-with-odbc-connection-pooling"></a>Uso de RDS con la agrupación de conexiones de ODBC


**Se aplica a:** Access 2013, Office 2013

Si está utilizando un origen de datos ODBC, puede utilizar la opción de agrupamiento de conexiones de Internet Information Services (IIS) para conseguir un gran rendimiento en el procesamiento de la carga de clientes. El agrupamiento de conexiones es un administrador de recursos para conexiones que mantiene el estado abierto en conexiones utilizadas con frecuencia.

Para habilitar el agrupamiento de conexiones, consulte la documentación de Internet Information Services.

Tenga en cuenta que la habilitación de la agrupación de conexiones puede someter el servidor web a otras restricciones, como se indica en la Microsoft Internet Information Services web.

Para garantizar que el agrupamiento de conexiones sea estable y proporcione mejoras de rendimiento adicionales, deberá configurar Microsoft SQL Server de modo que utilice la biblioteca de red de Sockets TCP/IP.

Para ello, deberá:

  - Configurar el equipo de SQL Server para utilizar sockets TCP/IP.

  - Configure el servidor web para que use sockets TCP/IP.

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a>Configurar el equipo de SQL Server para utilizar sockets TCP/IP

En el equipo de SQL Server, utilice el programa de configuración de SQL Server de modo que las interacciones con el origen de datos usen la biblioteca de red de Sockets TCP/IP.

**Para especificar la biblioteca de red de Sockets TCP/IP en el equipo de SQL Server**

**En Microsoft SQL Server 6.5:**

1.  En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 6.5** y, a continuación, haga clic en **Instalar SQL**.

2.  Haga clic dos veces en **Continuar**.

3.  En el cuadro de diálogo **Microsoft SQL Server  — Opciones**, seleccione **Cambiar soporte de red** y, a continuación, haga clic en **Continuar**.

4.  Asegúrese de que la casilla de verificación **Sockets TCP/IP** está activada y, a continuación, haga clic en **Aceptar**.

5.  Haga clic en **Continuar** para terminar y salga del programa de instalación.

**En Microsoft SQL Server 7.0:**

1.  En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 7.0** y, a continuación, haga clic en **Herramientas de red de SQL Server**.

2.  En la pestaña **General** del cuadro de diálogo, haga clic en **Agregar**.

3.  En el cuadro de diálogo **Agregar configuración de biblioteca de red**, haga clic en **TCP/IP**.

4.  En los cuadro de texto **Número de puerto** y **Dirección de proxy**, escriba el número de puerto y la dirección de proxy proporcionados por su administrador de red.

5.  Haga clic en **Aceptar** para terminar y salga del programa de instalación.

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a>Configuración del servidor web para usar sockets TCP/IP

Existen dos opciones para configurar el servidor web para que use sockets TCP/IP. Lo que haga depende de si se tiene acceso a todos los servidores SQL desde el servidor web o solo se tiene acceso a SQL Server específico desde el servidor web.

Si se tiene SQL todos los servidores desde el servidor web, debe ejecutar la utilidad de configuración SQL Server cliente en el equipo del servidor web. Los pasos siguientes cambian la biblioteca de red predeterminada para todas las SQL Server realizadas desde este servidor web iis para usar la biblioteca de red de sockets TCP/IP.

**Para configurar el servidor web (todos SQL servidores)**

**En Microsoft SQL Server 6.5:**

1.  En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 6.5** y, a continuación, haga clic en **Herramienta de configuración de clientes SQL**.

2.  Haga clic en la pestaña **Biblioteca de red**.

3.  En el cuadro **Red predeterminada**, seleccione **Sockets TCP/IP**.

4.  Haga clic en **Listo** para guardar los cambios y salir de la utilidad.

**En Microsoft SQL Server 7.0:**

1.  En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 7.0** y, a continuación, haga clic en **Herramientas de red de cliente**.

2.  Haga clic en la pestaña **General**.

3.  En el cuadro **Biblioteca de red predeterminada**, haga clic en **TCP/IP**.

4.  Haga clic en **Aceptar** para guardar los cambios y salir de la utilidad.

Si se tiene SQL Server un servidor web, debe ejecutar la utilidad de configuración de cliente SQL Server en el equipo del servidor web. Para cambiar la biblioteca de red para una conexión SQL Server, configure el software SQL Server cliente en el equipo servidor web de la siguiente manera.

**Para configurar el servidor web (un servidor SQL Server)**

**En Microsoft SQL Server 6.5:**

1.  En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 6.5** y, a continuación, haga clic en **Herramienta de configuración de clientes SQL**.

2.  Haga clic en la pestaña **Avanzadas**.

3.  En el cuadro **Servidor**, escriba el nombre del servidor con el que se va a conectar para usar **Sockets TCP/IP**.

4.  En el cuadro **Nombre de DLL**, seleccione **Sockets TCP/IP**.

5.  Haga clic en **Agregar o modificar**. Todos los orígenes de datos que apuntan a este servidor utilizarán ahora sockets TCP/IP.

6.  Haga clic en **Listo**.

**En Microsoft SQL Server 7.0:**

1.  En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 7.0** y, a continuación, haga clic en **Herramienta de configuración de clientes**.

2.  Haga clic en la pestaña **General**.

3.  Haga clic en **Agregar**.

4.  Escriba el alias del servidor en el cuadro **Alias del servidor**. En el cuadro **Bibliotecas de red**, haga clic en **TCP/IP**. En el cuadro **Nombre del equipo**, escriba el nombre del equipo que escucha clientes de sockets TCP/IP. En el cuadro **Número de puerto**, escriba el puerto en el que escucha el servidor SQL Server.

5.  Haga clic en **Aceptar** y, a continuación, de nuevo en **Aceptar** para salir de la utilidad.

