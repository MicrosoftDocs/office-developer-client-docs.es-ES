---
title: Append (método, procedimientos ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef11c9d45cc5b34b5ef7b1cf762dfd6f3e4c1d64
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873050"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="6587e-102">Append (método, procedimientos ADOX)</span><span class="sxs-lookup"><span data-stu-id="6587e-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="6587e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6587e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="6587e-104">Agrega un nuevo objeto [Procedure](procedure-object-adox.md) a la colección [Procedures](procedures-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6587e-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6587e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6587e-105">Syntax</span></span>

<span data-ttu-id="6587e-106">*Los procedimientos*. Anexe el*nombre*, *comando*</span><span class="sxs-lookup"><span data-stu-id="6587e-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="6587e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6587e-107">Parameters</span></span>

  - <span data-ttu-id="6587e-108">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="6587e-108">*Name*</span></span>

  - <span data-ttu-id="6587e-109">Un valor **String** que especifica el nombre del procedimiento que se va a crear y anexar.</span><span class="sxs-lookup"><span data-stu-id="6587e-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="6587e-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="6587e-110">*Command*</span></span>

  - <span data-ttu-id="6587e-111">Un objeto [Command](command-object-ado.md) de ADO que representa el procedimiento que se va a crear y anexar.</span><span class="sxs-lookup"><span data-stu-id="6587e-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="6587e-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6587e-112">Remarks</span></span>

<span data-ttu-id="6587e-113">Crea un procedimiento nuevo en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="6587e-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="6587e-p101">Si el texto del comando que especifica el usuario representa una vista en vez de un procedimiento, el comportamiento dependerá del proveedor que se utilice. Se producirá un error en **Append** si el proveedor no admite comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="6587e-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="6587e-116">Cuando se usa el proveedor OLE DB para Microsoft Jet, el método **Append** de la colección de **procedimientos** le permitirá especificar una **vista** en lugar de un **procedimiento** en el parámetro *Command* .</span><span class="sxs-lookup"><span data-stu-id="6587e-116">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="6587e-117">La **vista** se agregará al origen de datos y a la colección **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="6587e-117">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="6587e-118">Después del proceso **Append**, si se actualizan las colecciones **Procedures** y **Views**, la **vista** ya no existirá en la colección **Procedures** y aparecerá en la colección **Views**.</span><span class="sxs-lookup"><span data-stu-id="6587e-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


