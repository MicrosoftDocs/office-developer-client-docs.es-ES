---
title: Propiedad Database.Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9aecffc135ab402f02b8fd4e1cc234f4a6eb37d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927329"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="dfa7f-102">Propiedad Database.Connection (DAO)</span><span class="sxs-lookup"><span data-stu-id="dfa7f-102">Database.Connection property (DAO)</span></span>


<span data-ttu-id="dfa7f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfa7f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa7f-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfa7f-104">Syntax</span></span>

<span data-ttu-id="dfa7f-105">*expresión* . Conexión</span><span class="sxs-lookup"><span data-stu-id="dfa7f-105">*expression* .Connection</span></span>

<span data-ttu-id="dfa7f-106">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="dfa7f-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfa7f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfa7f-107">Remarks</span></span>

<span data-ttu-id="dfa7f-p101">Use la propiedad **Connection** para obtener una referencia a un objeto **Connection** que corresponda al objeto **Database**. En DAO, un objeto **Connection** y su objeto **Database** correspondiente son simplemente dos referencias diferentes de variable de objeto al mismo objeto. La propiedad **[Database](connection-database-property-dao.md)** de un objeto **Connection** y la propiedad **Connection** de un objeto **Database** facilitan el cambio de conexión a un origen de datos ODBC mediante el motor de base de datos de Microsoft Access para utilizar ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="dfa7f-p101">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

