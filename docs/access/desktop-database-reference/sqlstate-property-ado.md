---
title: SQLState (propiedad, ADO)
TOCTitle: SQLState Property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aead95e4276d61d69ae6ba5a86974cbe630f9043
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484989"
---
# <a name="sqlstate-property-ado"></a><span data-ttu-id="be311-102">SQLState (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="be311-102">SQLState Property (ADO)</span></span>


<span data-ttu-id="be311-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="be311-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="be311-104">Indica el estado SQL de un objeto [Error](error-object-ado.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="be311-104">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="be311-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be311-105">Return Value</span></span>

<span data-ttu-id="be311-106">Devuelve un valor de cinco caracteres de tipo **String** que sigue el estándar ANSI SQL e indica el código del error.</span><span class="sxs-lookup"><span data-stu-id="be311-106">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be311-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be311-107">Remarks</span></span>

<span data-ttu-id="be311-p101">Use la propiedad **SQLState** para leer el código de error de cinco caracteres que devuelve el proveedor cuando se produce un error durante el procesamiento de una instrucción SQL. Por ejemplo, cuando se usa el Proveedor de Microsoft OLE DB para ODBC con una base de datos de Microsoft SQL Server, los códigos de error de estado SQL se originan en ODBC, basándose en errores específicos de ODBC o en errores que se originan en Microsoft SQL Server, y se asignan a errores ODBC. Estos códigos de error están documentados en el estándar ANSI de SQL, pero pueden ser implementados de formas diferentes por los distintos orígenes de datos.</span><span class="sxs-lookup"><span data-stu-id="be311-p101">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement. For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors. These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>
