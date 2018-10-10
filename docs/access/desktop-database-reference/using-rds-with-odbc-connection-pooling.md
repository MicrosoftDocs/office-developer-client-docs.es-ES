---
title: Utilizar RDS con agrupamiento de conexiones ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7baaf81d7a5d6a91416ea5baf8ba57745612740e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483680"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="181b6-102">Utilizar RDS con agrupamiento de conexiones ODBC</span><span class="sxs-lookup"><span data-stu-id="181b6-102">Using RDS with ODBC Connection Pooling</span></span>


<span data-ttu-id="181b6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="181b6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="181b6-p101">Si está utilizando un origen de datos ODBC, puede utilizar la opción de agrupamiento de conexiones de Internet Information Services (IIS) para conseguir un gran rendimiento en el procesamiento de la carga de clientes. El agrupamiento de conexiones es un administrador de recursos para conexiones que mantiene el estado abierto en conexiones utilizadas con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="181b6-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="181b6-106">Para habilitar el agrupamiento de conexiones, consulte la documentación de Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="181b6-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="181b6-107">Observe que, si habilita el agrupamiento de conexiones, puede someter el servidor web a otras restricciones, como se indica en la documentación de Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="181b6-107">Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="181b6-108">Para garantizar que el agrupamiento de conexiones sea estable y proporcione mejoras de rendimiento adicionales, deberá configurar Microsoft SQL Server de modo que utilice la biblioteca de red de Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="181b6-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="181b6-109">Para ello, deberá:</span><span class="sxs-lookup"><span data-stu-id="181b6-109">To do this, you need to:</span></span>

  - <span data-ttu-id="181b6-110">Configurar el equipo de SQL Server para utilizar sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="181b6-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="181b6-111">Configurar el servidor Web para utilizar sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="181b6-111">Configure the Web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="181b6-112">Configurar el equipo de SQL Server para utilizar sockets TCP/IP</span><span class="sxs-lookup"><span data-stu-id="181b6-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="181b6-113">En el equipo de SQL Server, utilice el programa de configuración de SQL Server de modo que las interacciones con el origen de datos usen la biblioteca de red de Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="181b6-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="181b6-114">**Para especificar la biblioteca de red de Sockets TCP/IP en el equipo de SQL Server**</span><span class="sxs-lookup"><span data-stu-id="181b6-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="181b6-115">**En Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="181b6-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="181b6-116">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 6.5** y, a continuación, haga clic en **Instalar SQL**.</span><span class="sxs-lookup"><span data-stu-id="181b6-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="181b6-117">Haga clic dos veces en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="181b6-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="181b6-118">En el cuadro de diálogo **Microsoft SQL Server  Opciones**, seleccione **Cambiar soporte de red** y, a continuación, haga clic en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="181b6-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="181b6-119">Asegúrese de que la casilla de verificación **Sockets TCP/IP** está activada y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="181b6-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="181b6-120">Haga clic en **Continuar** para terminar y salga del programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="181b6-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="181b6-121">**En Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="181b6-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="181b6-122">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 7.0** y, a continuación, haga clic en **Herramientas de red de SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="181b6-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="181b6-123">En la pestaña **General** del cuadro de diálogo, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="181b6-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="181b6-124">En el cuadro de diálogo **Agregar configuración de biblioteca de red**, haga clic en \*\* TCP/IP\*\*.</span><span class="sxs-lookup"><span data-stu-id="181b6-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="181b6-125">En los cuadro de texto **Número de puerto** y **Dirección de proxy**, escriba el número de puerto y la dirección de proxy proporcionados por su administrador de red.</span><span class="sxs-lookup"><span data-stu-id="181b6-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="181b6-126">Haga clic en **Aceptar** para terminar y salga del programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="181b6-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="181b6-127">Configurar el servidor Web para utilizar sockets TCP/IP</span><span class="sxs-lookup"><span data-stu-id="181b6-127">Configuring the Web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="181b6-p102">Existen dos opciones para configurar el servidor Web de modo que utilice sockets TCP/IP. La elección depende de si el acceso a todos los servidores SQL Server se realiza desde el servidor Web o si el acceso es sólo a un servidor SQL Server específico.</span><span class="sxs-lookup"><span data-stu-id="181b6-p102">There are two options for configuring the Web server to use TCP/IP Sockets. What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</span></span>

<span data-ttu-id="181b6-p103">Si el acceso a todos los servidores SQL Server se realiza desde el servidor Web, deberá ejecutar la Utilidad de Configuración de cliente de SQL Server en el equipo del servidor Web. Los siguientes pasos cambian la biblioteca de red predeterminada para todas las conexiones de SQL Server procedentes de este servidor Web de IIS de modo que utilicen la biblioteca de red de sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="181b6-p103">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="181b6-132">**Para configurar el servidor Web (todos los servidores SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="181b6-132">**To configure the Web server (all SQL Servers)**</span></span>

<span data-ttu-id="181b6-133">**En Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="181b6-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="181b6-134">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 6.5** y, a continuación, haga clic en **Herramienta de configuración de clientes SQL**.</span><span class="sxs-lookup"><span data-stu-id="181b6-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="181b6-135">Haga clic en la pestaña **Biblioteca de red**.</span><span class="sxs-lookup"><span data-stu-id="181b6-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="181b6-136">En el cuadro **Red predeterminada**, seleccione **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="181b6-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="181b6-137">Haga clic en **Listo** para guardar los cambios y salir de la utilidad.</span><span class="sxs-lookup"><span data-stu-id="181b6-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="181b6-138">**En Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="181b6-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="181b6-139">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 7.0** y, a continuación, haga clic en **Herramientas de red de cliente**.</span><span class="sxs-lookup"><span data-stu-id="181b6-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="181b6-140">Haga clic en la pestaña **General**.</span><span class="sxs-lookup"><span data-stu-id="181b6-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="181b6-141">En el cuadro **Biblioteca de red predeterminada**, haga clic en **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="181b6-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="181b6-142">Haga clic en **Aceptar** para guardar los cambios y salir de la utilidad.</span><span class="sxs-lookup"><span data-stu-id="181b6-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="181b6-p104">Si el acceso a un servidor SQL Server específico se realiza desde un servidor Web, deberá ejecutar la Utilidad de configuración de cliente de SQL Server en el equipo del servidor Web. Para cambiar la biblioteca de red para una conexión específica de SQL Server, configure el software del cliente de SQL Server en el equipo del servidor Web del siguiente modo.</span><span class="sxs-lookup"><span data-stu-id="181b6-p104">If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</span></span>

<span data-ttu-id="181b6-145">**Para configurar el servidor Web (un servidor SQL Server específico)**</span><span class="sxs-lookup"><span data-stu-id="181b6-145">**To configure the Web server (a specific SQL Server)**</span></span>

<span data-ttu-id="181b6-146">**En Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="181b6-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="181b6-147">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 6.5** y, a continuación, haga clic en **Herramienta de configuración de clientes SQL**.</span><span class="sxs-lookup"><span data-stu-id="181b6-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="181b6-148">Haga clic en la pestaña **Avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="181b6-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="181b6-149">En el cuadro **Servidor**, escriba el nombre del servidor con el que se va a conectar para usar **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="181b6-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="181b6-150">En el cuadro **Nombre de DLL**, seleccione **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="181b6-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="181b6-p105">Haga clic en **Agregar o modificar**. Todos los orígenes de datos que apuntan a este servidor utilizarán ahora sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="181b6-p105">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="181b6-153">Haga clic en **Listo**.</span><span class="sxs-lookup"><span data-stu-id="181b6-153">Click **Done**.</span></span>

<span data-ttu-id="181b6-154">**En Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="181b6-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="181b6-155">En el menú **Inicio**, elija **Programas**, **Microsoft SQL Server 7.0** y, a continuación, haga clic en **Herramienta de configuración de clientes**.</span><span class="sxs-lookup"><span data-stu-id="181b6-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="181b6-156">Haga clic en la pestaña **General**.</span><span class="sxs-lookup"><span data-stu-id="181b6-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="181b6-157">Haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="181b6-157">Click **Add**.</span></span>

4.  <span data-ttu-id="181b6-p106">Escriba el alias del servidor en el cuadro **Alias del servidor**. En el cuadro **Bibliotecas de red**, haga clic en **TCP/IP**. En el cuadro **Nombre del equipo**, escriba el nombre del equipo que escucha clientes de sockets TCP/IP. En el cuadro **Número de puerto**, escriba el puerto en el que escucha el servidor SQL Server.</span><span class="sxs-lookup"><span data-stu-id="181b6-p106">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="181b6-162">Haga clic en **Aceptar** y, a continuación, de nuevo en **Aceptar** para salir de la utilidad.</span><span class="sxs-lookup"><span data-stu-id="181b6-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

