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
# <a name="data-providers"></a>Proveedores de datos


**Se aplica a:** Access 2013, Office 2013

Los proveedores de datos representan diversos orígenes de datos como bases de datos SQL, archivos secuenciales indizados, hojas de cálculo, almacenes de documentos y archivos de correo. Los proveedores exponen datos uniformemente mediante una abstracción común que se denomina conjunto de filas.

ADO es eficaz y flexible porque puede conectarse a cualquiera entre varios proveedores de datos y seguir exponiendo el mismo modelo de programación, independientemente de las características específicas de un proveedor determinado. No obstante, dado que cada proveedor de datos es único, la interacción de una aplicación con ADO variará según cuál sea el proveedor de datos.

Por ejemplo, las capacidades y características del proveedor OLE DB para SQL Server, que se usa para tener acceso a bases de datos de Microsoft SQL Server, son considerablemente diferentes de las del proveedor ole db de Microsoft para la publicación en Internet, que se usa para tener acceso a los almacenes de archivos en un servidor web.

