---
title: Proveedores de datos (referencia de base de datos de escritorio de Access)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 46d9cf80bfdd15f48d876fe63a617c9b30931fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295068"
---
# <a name="data-providers"></a><span data-ttu-id="5a5a6-102">Proveedores de datos</span><span class="sxs-lookup"><span data-stu-id="5a5a6-102">Data providers</span></span>


<span data-ttu-id="5a5a6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a5a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a5a6-p101">Los proveedores de datos representan diversos orígenes de datos como bases de datos SQL, archivos secuenciales indizados, hojas de cálculo, almacenes de documentos y archivos de correo. Los proveedores exponen datos uniformemente mediante una abstracción común que se denomina conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="5a5a6-p101">Data providers represent diverse sources of data such as SQL databases, indexed-sequential files, spreadsheets, document stores, and mail files. Providers expose data uniformly using a common abstraction called the rowset.</span></span>

<span data-ttu-id="5a5a6-p102">ADO es eficaz y flexible porque puede conectarse a cualquiera entre varios proveedores de datos y seguir exponiendo el mismo modelo de programación, independientemente de las características específicas de un proveedor determinado. No obstante, dado que cada proveedor de datos es único, la interacción de una aplicación con ADO variará según cuál sea el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="5a5a6-p102">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider. However, because each data provider is unique, how your application interacts with ADO will vary by data provider.</span></span>

<span data-ttu-id="5a5a6-108">Por ejemplo, las capacidades y características del proveedor OLE DB para SQL Server, que se usa para tener acceso a las bases de datos de Microsoft SQL Server, son considerablemente diferentes de las de Microsoft OLE DB Provider for Internet Publishing, que se usa para obtener acceso al archivo almacena en un servidor Web.</span><span class="sxs-lookup"><span data-stu-id="5a5a6-108">For example, the capabilities and features of the OLE DB Provider for SQL Server, which is used to access Microsoft SQL Server databases, are considerably different from those of the Microsoft OLE DB Provider for Internet Publishing, which is used to access file stores on a web server.</span></span>

