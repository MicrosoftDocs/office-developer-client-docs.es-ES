---
title: Escenario de persistencia del objeto Recordset XML
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bbb8a3aa50027be7ce025a04d5987a45fee888f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486186"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="fc941-102">Escenario de persistencia del objeto Recordset XML</span><span class="sxs-lookup"><span data-stu-id="fc941-102">XML Recordset Persistence Scenario</span></span>


<span data-ttu-id="fc941-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc941-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="fc941-104">Escenario de persistencia del objeto Recordset XML</span><span class="sxs-lookup"><span data-stu-id="fc941-104">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="fc941-105">En este escenario, creará una aplicación de páginas ASP que guarda el contenido de un objeto **Recordset** directamente en el objeto **Response** de ASP.</span><span class="sxs-lookup"><span data-stu-id="fc941-105">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fc941-106">[!NOTA] Este escenario requiere que el servidor tenga instalado Internet Information Server 5.0 (IIS) o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="fc941-106">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span></P>



<span data-ttu-id="fc941-107">El objeto **Recordset** devuelto se muestra en Internet Explorer mediante un [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="fc941-107">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="fc941-108">Para crear el escenario, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="fc941-108">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="fc941-109">Configurar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc941-109">Set up the application.</span></span>

2.  <span data-ttu-id="fc941-110">Obtener los datos.</span><span class="sxs-lookup"><span data-stu-id="fc941-110">Get the data.</span></span>

3.  <span data-ttu-id="fc941-111">Enviar los datos.</span><span class="sxs-lookup"><span data-stu-id="fc941-111">Send the data.</span></span>

4.  <span data-ttu-id="fc941-112">Recibir y mostrar los datos.</span><span class="sxs-lookup"><span data-stu-id="fc941-112">Receive and display the data.</span></span>

<span data-ttu-id="fc941-113">**Siguiente**[Paso 1: Configurar la aplicación](step-1-set-up-the-application.md)</span><span class="sxs-lookup"><span data-stu-id="fc941-113">**Next**[Step 1: Set Up the Application](step-1-set-up-the-application.md)</span></span>

