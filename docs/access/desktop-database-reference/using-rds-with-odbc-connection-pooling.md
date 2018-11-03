---
title: Utilizar RDS con agrupamiento de conexiones ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35a4327a76ff34f503c988e8d51f5aa73d6c454b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946723"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="70a8e-102">Utilizar RDS con agrupamiento de conexiones ODBC</span><span class="sxs-lookup"><span data-stu-id="70a8e-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="70a8e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70a8e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70a8e-p101">Si está utilizando un origen de datos ODBC, puede utilizar la opción de agrupamiento de conexiones de Internet Information Services (IIS) para conseguir un gran rendimiento en el procesamiento de la carga de clientes. El agrupamiento de conexiones es un administrador de recursos para conexiones que mantiene el estado abierto en conexiones utilizadas con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="70a8e-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="70a8e-106">Para habilitar el agrupamiento de conexiones, consulte la documentación de Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="70a8e-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="70a8e-107">Tenga en cuenta que si habilita el agrupamiento de conexión puede sujeto al servidor web a otras restricciones, como se indicó en la documentación de Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="70a8e-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="70a8e-108">Para garantizar que el agrupamiento de conexiones sea estable y proporcione mejoras de rendimiento adicionales, deberá configurar Microsoft SQL Server de modo que utilice la biblioteca de red de Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="70a8e-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="70a8e-109">Para ello, deberá:</span><span class="sxs-lookup"><span data-stu-id="70a8e-109">To do this, you need to:</span></span>

  - <span data-ttu-id="70a8e-110">Configurar el equipo de SQL Server para utilizar sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="70a8e-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="70a8e-111">Configurar el servidor web para utilizar Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="70a8e-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="70a8e-112">Configurar el equipo de SQL Server para utilizar sockets TCP/IP</span><span class="sxs-lookup"><span data-stu-id="70a8e-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="70a8e-113">En el equipo de SQL Server, utilice el programa de configuración de SQL Server de modo que las interacciones con el origen de datos usen la biblioteca de red de Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="70a8e-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="70a8e-114">**Para especificar la biblioteca de red de Sockets TCP/IP en el equipo de SQL Server**</span><span class="sxs-lookup"><span data-stu-id="70a8e-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="70a8e-115">**En Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="70a8e-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="70a8e-116">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 6.5** y, a continuación, haga clic en **Instalar SQL**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="70a8e-117">Haga clic dos veces en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="70a8e-118">En el cuadro de diálogo **Microsoft SQL Server  Opciones**, seleccione **Cambiar soporte de red** y, a continuación, haga clic en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="70a8e-119">Asegúrese de que la casilla de verificación **Sockets TCP/IP** está activada y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="70a8e-120">Haga clic en **Continuar** para terminar y salga del programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="70a8e-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="70a8e-121">**En Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="70a8e-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="70a8e-122">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 7.0** y, a continuación, haga clic en **Herramientas de red de SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="70a8e-123">En la pestaña **General** del cuadro de diálogo, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="70a8e-124">En el cuadro de diálogo **Agregar configuración de biblioteca de red**, haga clic en \*\* TCP/IP\*\*.</span><span class="sxs-lookup"><span data-stu-id="70a8e-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="70a8e-125">En los cuadro de texto **Número de puerto** y **Dirección de proxy**, escriba el número de puerto y la dirección de proxy proporcionados por su administrador de red.</span><span class="sxs-lookup"><span data-stu-id="70a8e-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="70a8e-126">Haga clic en **Aceptar** para terminar y salga del programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="70a8e-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="70a8e-127">Configurar el servidor para usar TCP/IP Sockets de web</span><span class="sxs-lookup"><span data-stu-id="70a8e-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="70a8e-128">Hay dos opciones para configurar el servidor web para utilizar Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="70a8e-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="70a8e-129">¿Qué depende de si se tiene acceso a todos los servidores de SQL Server desde el servidor web o sólo un servidor SQL Server específico se obtiene acceso desde el servidor web.</span><span class="sxs-lookup"><span data-stu-id="70a8e-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="70a8e-130">Si se tiene acceso a todos los servidores de SQL Server desde el servidor web, debe ejecutar la utilidad de configuración de cliente de SQL Server en el equipo servidor web.</span><span class="sxs-lookup"><span data-stu-id="70a8e-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="70a8e-131">Los siguientes pasos cambian la biblioteca de red predeterminada para todas las conexiones de SQL Server realizadas desde el servidor web de IIS para usar la biblioteca de red de Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="70a8e-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="70a8e-132">**Para configurar el servidor web (todos los servidores de SQL)**</span><span class="sxs-lookup"><span data-stu-id="70a8e-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="70a8e-133">**En Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="70a8e-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="70a8e-134">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 6.5** y, a continuación, haga clic en **Herramienta de configuración de clientes SQL**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="70a8e-135">Haga clic en la pestaña **Biblioteca de red**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="70a8e-136">En el cuadro **Red predeterminada**, seleccione **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="70a8e-137">Haga clic en **Listo** para guardar los cambios y salir de la utilidad.</span><span class="sxs-lookup"><span data-stu-id="70a8e-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="70a8e-138">**En Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="70a8e-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="70a8e-139">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 7.0** y, a continuación, haga clic en **Herramientas de red de cliente**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="70a8e-140">Haga clic en la pestaña **General**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="70a8e-141">En el cuadro **Biblioteca de red predeterminada**, haga clic en **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="70a8e-142">Haga clic en **Aceptar** para guardar los cambios y salir de la utilidad.</span><span class="sxs-lookup"><span data-stu-id="70a8e-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="70a8e-143">Si se obtiene acceso a un servidor SQL Server específico desde un servidor web, debe ejecutar la utilidad de configuración de cliente de SQL Server en el equipo servidor web.</span><span class="sxs-lookup"><span data-stu-id="70a8e-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="70a8e-144">Para cambiar la biblioteca de red para una conexión específica de SQL Server, configure el software de cliente de SQL Server en el equipo servidor web.</span><span class="sxs-lookup"><span data-stu-id="70a8e-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="70a8e-145">**Para configurar el servidor web (un servidor SQL Server específico)**</span><span class="sxs-lookup"><span data-stu-id="70a8e-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="70a8e-146">**En Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="70a8e-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="70a8e-147">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 6.5** y, a continuación, haga clic en **Herramienta de configuración de clientes SQL**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="70a8e-148">Haga clic en la pestaña **Avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="70a8e-149">En el cuadro **Servidor**, escriba el nombre del servidor con el que se va a conectar para usar **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="70a8e-150">En el cuadro **Nombre de DLL**, seleccione **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="70a8e-p105">Haga clic en **Agregar o modificar**. Todos los orígenes de datos que apuntan a este servidor utilizarán ahora sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="70a8e-p105">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="70a8e-153">Haga clic en **Listo**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-153">Click **Done**.</span></span>

<span data-ttu-id="70a8e-154">**En Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="70a8e-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="70a8e-155">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 7.0** y, a continuación, haga clic en **Herramienta de configuración de clientes**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="70a8e-156">Haga clic en la pestaña **General**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="70a8e-157">Haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="70a8e-157">Click **Add**.</span></span>

4.  <span data-ttu-id="70a8e-p106">Escriba el alias del servidor en el cuadro **Alias del servidor**. En el cuadro **Bibliotecas de red**, haga clic en **TCP/IP**. En el cuadro **Nombre del equipo**, escriba el nombre del equipo que escucha clientes de sockets TCP/IP. En el cuadro **Número de puerto**, escriba el puerto en el que escucha el servidor SQL Server.</span><span class="sxs-lookup"><span data-stu-id="70a8e-p106">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="70a8e-162">Haga clic en **Aceptar** y, a continuación, de nuevo en **Aceptar** para salir de la utilidad.</span><span class="sxs-lookup"><span data-stu-id="70a8e-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

