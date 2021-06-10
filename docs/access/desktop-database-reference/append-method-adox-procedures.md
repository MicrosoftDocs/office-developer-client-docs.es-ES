---
title: Append (método, Procedures de ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297084"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="5b6f0-102">Append (método, Procedures de ADOX)</span><span class="sxs-lookup"><span data-stu-id="5b6f0-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="5b6f0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b6f0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b6f0-104">Agrega un nuevo objeto [Procedure](procedure-object-adox.md) a la colección [Procedures](procedures-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5b6f0-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b6f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b6f0-105">Syntax</span></span>

<span data-ttu-id="5b6f0-106">*Procedimientos*. Append *Name*, *Command*</span><span class="sxs-lookup"><span data-stu-id="5b6f0-106">*Procedures*.Append *Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="5b6f0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b6f0-107">Parameters</span></span>

|<span data-ttu-id="5b6f0-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5b6f0-108">Parameter</span></span>|<span data-ttu-id="5b6f0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b6f0-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5b6f0-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="5b6f0-110">*Name*</span></span> |<span data-ttu-id="5b6f0-111">Un valor **String** que especifica el nombre del procedimiento que se va a crear y anexar.</span><span class="sxs-lookup"><span data-stu-id="5b6f0-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="5b6f0-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="5b6f0-112">*Command*</span></span> |<span data-ttu-id="5b6f0-113">Un objeto [Command](command-object-ado.md) de ADO que representa el procedimiento que se va a crear y anexar.</span><span class="sxs-lookup"><span data-stu-id="5b6f0-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5b6f0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b6f0-114">Remarks</span></span>

<span data-ttu-id="5b6f0-115">Crea un procedimiento nuevo en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="5b6f0-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="5b6f0-p101">Si el texto del comando que especifica el usuario representa una vista en vez de un procedimiento, el comportamiento dependerá del proveedor que se utilice. Se producirá un error en **Append** si el proveedor no admite comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="5b6f0-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="5b6f0-p102">Cuando se utiliza OLE DB Provider para Microsoft Jet, el método **Append** de la colección **Procedures** permite especificar una **vista** en lugar de un **procedimiento** en el parámetro *Command*. La **vista** se agregará al origen de datos y a la colección **Procedures**. Después del proceso **Append**, si se actualizan las colecciones **Procedures** y **Views**, la **vista** ya no existirá en la colección **Procedures** y aparecerá en la colección **Views**.</span><span class="sxs-lookup"><span data-stu-id="5b6f0-p102">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter. The **View** will be added to the data source and will be added to the **Procedures** collection. After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


