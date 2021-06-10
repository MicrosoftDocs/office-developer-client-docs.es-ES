---
title: Soluciones para el acceso remoto a datos
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b64ed19c268874e0e52a87bc2e05aacb6083422
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306905"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="4f3f4-102">Soluciones para el acceso a datos remotos</span><span class="sxs-lookup"><span data-stu-id="4f3f4-102">Solutions for Remote Data Access</span></span>

<span data-ttu-id="4f3f4-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f3f4-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="4f3f4-104">El problema</span><span class="sxs-lookup"><span data-stu-id="4f3f4-104">The issue</span></span>

<span data-ttu-id="4f3f4-p101">ADO habilita la aplicación para obtener acceso directo y modificar orígenes de datos (a veces se denomina sistema de dos niveles).

Por ejemplo, si hay una conexión con el origen de datos que contiene los datos, se trata de una conexión directa en un sistema de dos niveles.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-p101">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system). For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="4f3f4-107">Sin embargo, es posible que desee tener acceso a orígenes de datos indirectamente a través de un intermediario como Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="4f3f4-107">However, you may want to access data sources indirectly through an intermediary such as Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="4f3f4-108">Esto se denomina a veces un sistema de tres niveles.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-108">This arrangement is sometimes called a three-tier system.</span></span> <span data-ttu-id="4f3f4-109">IIS es un sistema de cliente/servidor que permite de manera eficaz que una aplicación local o de cliente invoque un programa remoto o de servidor a través de Internet o una intranet.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-109">IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</span></span> <span data-ttu-id="4f3f4-110">El programa de servidor obtiene acceso al origen de datos y procesa opcionalmente los datos adquiridos.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-110">The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="4f3f4-111">Por ejemplo, la página web de intranet contiene una aplicación escrita en Microsoft Visual Basic Scripting Edition (VBScript), que se conecta a IIS.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-111">For example, your intranet webpage contains an application written in Microsoft Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="4f3f4-112">IIS se conecta a su vez al origen de datos real, recupera los datos, los procesa de alguna manera y, a continuación, devuelve la información procesada a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>

<span data-ttu-id="4f3f4-p104">En este ejemplo, la aplicación no se ha conectado en ningún momento directamente al origen de datos. IIS se ha encargado de esa conexión y ha obtenido acceso a los datos por medio de ADO.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-p104">In this example, your application never directly connected to the data source; IIS did. And IIS accessed the data by means of ADO.</span></span>

> [!NOTE]
> <span data-ttu-id="4f3f4-115">La aplicación cliente/servidor no tiene que basarse en Internet ni en una intranet (es decir, basada en web), podría consistir únicamente en programas compilados en una red de área local.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-115">The client/server application does not have to be based on the Internet or an intranet (that is, web-based)—it could consist solely of compiled programs on a local area network.</span></span> <span data-ttu-id="4f3f4-116">Sin embargo, el caso típico es una aplicación basada en web.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-116">However, the typical case is a web-based application.</span></span>

<span data-ttu-id="4f3f4-117">Dado que algunos controles visuales, como una cuadrícula, una casilla de verificación o una lista, pueden utilizar la información devuelta, ésta debe ser fácilmente utilizable por los controles visuales.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-117">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="4f3f4-p106">Desea disponer de una interfaz de programación de aplicaciones simple y eficaz que admita sistemas de tres niveles y devuelva la información con la misma facilidad con la que se recupera en un sistema de dos niveles. El servicio de datos remotos (RDS) es esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-p106">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system. Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="4f3f4-120">Solución</span><span class="sxs-lookup"><span data-stu-id="4f3f4-120">The solution</span></span>

<span data-ttu-id="4f3f4-121">RDS define un modelo de programación (la secuencia de actividades necesarias para obtener acceso a un origen de datos y actualizarlo) para obtener acceso a los datos a través de un intermediario, como Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="4f3f4-121">RDS defines a programming model—the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS).</span></span> <span data-ttu-id="4f3f4-122">El modelo de programación resume toda la funcionalidad de RDS.</span><span class="sxs-lookup"><span data-stu-id="4f3f4-122">The programming model summarizes the entire functionality of RDS.</span></span>

