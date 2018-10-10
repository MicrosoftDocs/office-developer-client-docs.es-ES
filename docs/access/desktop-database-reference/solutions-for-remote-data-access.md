---
title: Soluciones para el acceso remoto a datos
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6e9bf0cfd27e478b66ccc046412c0e874a4ebd6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486822"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="b2cd5-102">Soluciones para el acceso remoto a datos</span><span class="sxs-lookup"><span data-stu-id="b2cd5-102">Solutions for Remote Data Access</span></span>


<span data-ttu-id="b2cd5-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2cd5-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="b2cd5-104">Problema</span><span class="sxs-lookup"><span data-stu-id="b2cd5-104">The Issue</span></span>

<span data-ttu-id="b2cd5-p101">ADO habilita la aplicación para obtener acceso directo y modificar orígenes de datos (a veces se denomina sistema de dos niveles). Por ejemplo, si hay una conexión con el origen de datos que contiene los datos, se trata de una conexión directa en un sistema de dos niveles.</span><span class="sxs-lookup"><span data-stu-id="b2cd5-p101">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system). For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="b2cd5-p102">Sin embargo, es posible que desee obtener indirectamente acceso a los orígenes de datos a través de un intermediario como Internet Information Services de Microsoft® (IIS). Esto se denomina a veces un sistema de tres niveles. IIS es un sistema de cliente/servidor que permite de manera eficaz que una aplicación local o de cliente invoque un programa remoto o de servidor a través de Internet o una intranet. El programa de servidor obtiene acceso al origen de datos y procesa opcionalmente los datos adquiridos.</span><span class="sxs-lookup"><span data-stu-id="b2cd5-p102">However, you may want to access data sources indirectly through an intermediary such as Microsoft® Internet Information Services (IIS). This arrangement is sometimes called a three-tier system. IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet. The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="b2cd5-p103">Por ejemplo, una página Web de la intranet contiene una aplicación escrita en Microsoft® Visual Basic Scripting Edition (VBScript), que se conecta a IIS. IIS se conecta a su vez al origen de datos real, recupera los datos, los procesa de alguna manera y, a continuación, devuelve la información procesada a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2cd5-p103">For example, your intranet Web page contains an application written in Microsoft® Visual Basic Scripting Edition (VBScript), which connects to IIS. IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>

<span data-ttu-id="b2cd5-p104">En este ejemplo, la aplicación no se ha conectado en ningún momento directamente al origen de datos. IIS se ha encargado de esa conexión y ha obtenido acceso a los datos por medio de ADO.</span><span class="sxs-lookup"><span data-stu-id="b2cd5-p104">In this example, your application never directly connected to the data source; IIS did. And IIS accessed the data by means of ADO.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b2cd5-p105">[!NOTA] La aplicación de cliente/servidor no debe estar ubicada en Internet o una intranet (es decir, basada en Web). Puede constar únicamente de programas compilados en una red local. Sin embargo, normalmente se trata de una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="b2cd5-p105">The client/server application does not have to be based on the Internet or an intranet (that is, Web-based) — it could consist solely of compiled programs on a local area network. However, the typical case is a Web-based application.</span></span></P>



<span data-ttu-id="b2cd5-117">Dado que algunos controles visuales, como una cuadrícula, una casilla de verificación o una lista, pueden utilizar la información devuelta, ésta debe ser fácilmente utilizable por los controles visuales.</span><span class="sxs-lookup"><span data-stu-id="b2cd5-117">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="b2cd5-p106">Desea disponer de una interfaz de programación de aplicaciones simple y eficaz que admita sistemas de tres niveles y devuelva la información con la misma facilidad con la que se recupera en un sistema de dos niveles. El servicio de datos remotos (RDS) es esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="b2cd5-p106">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system. Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="b2cd5-120">Solución</span><span class="sxs-lookup"><span data-stu-id="b2cd5-120">The Solution</span></span>

<span data-ttu-id="b2cd5-p107">RDS define un modelo de programación (es decir, la secuencia de actividades necesarias para obtener acceso y actualizar un origen de datos) para obtener acceso a datos a través de un intermediario, como Internet Information Services (IIS). El modelo de programación resume toda la funcionalidad de RDS.</span><span class="sxs-lookup"><span data-stu-id="b2cd5-p107">RDS defines a programming model — the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS). The programming model summarizes the entire functionality of RDS.</span></span>

