---
title: NativeError (propiedad, ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 86734d77cafd8dbe3c26219e291c16b81ef0026b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288613"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="b0a7b-102">NativeError (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="b0a7b-102">NativeError property (ADO)</span></span>


<span data-ttu-id="b0a7b-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0a7b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0a7b-104">Indica el código de error específico de un proveedor para un objeto [Error](error-object-ado.md) dado.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0a7b-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0a7b-105">Return value</span></span>

<span data-ttu-id="b0a7b-106">Devuelve un valor de tipo **Long** que indica el código del error.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0a7b-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0a7b-107">Remarks</span></span>

<span data-ttu-id="b0a7b-p101">Utilice la propiedad **NativeError** para recuperar información de error específica de base de datos de un objeto **Error** concreto. Por ejemplo, al utilizar el Proveedor de Microsoft OLE DB para ODBC con una base de datos de Microsoft SQL Server, los códigos de error nativos que se originan en SQL Server pasan a través de ODBC y el Proveedor ODBC a la propiedad **NativeError** de ADO.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

