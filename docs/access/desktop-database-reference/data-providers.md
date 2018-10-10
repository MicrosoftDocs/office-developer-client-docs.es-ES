---
title: Proveedores de datos (referencia de escritorio de la base de datos de Access)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd2f17bcc490031625cc8f6cd0ea6d369133fa06
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484191"
---
# <a name="data-providers"></a><span data-ttu-id="4e834-102">Proveedores de datos</span><span class="sxs-lookup"><span data-stu-id="4e834-102">Data Providers</span></span>


<span data-ttu-id="4e834-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e834-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4e834-p101">Los proveedores de datos representan diversos orígenes de datos como bases de datos SQL, archivos secuenciales indizados, hojas de cálculo, almacenes de documentos y archivos de correo. Los proveedores exponen datos uniformemente mediante una abstracción común que se denomina conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="4e834-p101">Data providers represent diverse sources of data such as SQL databases, indexed-sequential files, spreadsheets, document stores, and mail files. Providers expose data uniformly using a common abstraction called the rowset.</span></span>

<span data-ttu-id="4e834-p102">ADO es eficaz y flexible porque puede conectarse a cualquiera entre varios proveedores de datos y seguir exponiendo el mismo modelo de programación, independientemente de las características específicas de un proveedor determinado. No obstante, dado que cada proveedor de datos es único, la interacción de una aplicación con ADO variará según cuál sea el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="4e834-p102">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider. However, because each data provider is unique, how your application interacts with ADO will vary by data provider.</span></span>

<span data-ttu-id="4e834-108">Por ejemplo, las funcionalidades y las características del proveedor OLE DB para SQL Server, que se utiliza para tener acceso a bases de datos de Microsoft SQL Server, son considerablemente diferentes de las correspondientes al proveedor de Microsoft OLE DB para Internet Publishing, que se utiliza para tener acceso a almacenes de archivo en un servidor Web.</span><span class="sxs-lookup"><span data-stu-id="4e834-108">For example, the capabilities and features of the OLE DB Provider for SQL Server, which is used to access Microsoft SQL Server databases, are considerably different from those of the Microsoft OLE DB Provider for Internet Publishing, which is used to access file stores on a Web server.</span></span>

