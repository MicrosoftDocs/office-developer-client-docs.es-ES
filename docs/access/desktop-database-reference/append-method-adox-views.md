---
title: Append (método, Views de ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716158"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="4b9a8-102">Append (método, Views de ADOX)</span><span class="sxs-lookup"><span data-stu-id="4b9a8-102">Append method (ADOX Views)</span></span>

<span data-ttu-id="4b9a8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b9a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b9a8-104">Crea un nuevo objeto [View](view-object-adox.md) y lo anexa a la colección [Views](views-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4b9a8-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b9a8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b9a8-105">Syntax</span></span>

<span data-ttu-id="4b9a8-106">*Las vistas*. Anexe el*nombre*, *comando*</span><span class="sxs-lookup"><span data-stu-id="4b9a8-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="4b9a8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b9a8-107">Parameters</span></span>

|<span data-ttu-id="4b9a8-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4b9a8-108">Parameter</span></span>|<span data-ttu-id="4b9a8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b9a8-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4b9a8-110">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="4b9a8-110">*Name*</span></span> |<span data-ttu-id="4b9a8-111">Un valor **String** que especifica el nombre de la vista que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="4b9a8-111">A **String** value that specifies the name of the view to create.</span></span>|
|<span data-ttu-id="4b9a8-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="4b9a8-112">*Command*</span></span> |<span data-ttu-id="4b9a8-113">Un objeto [Command](command-object-ado.md) de ADO que representa la vista que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="4b9a8-113">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4b9a8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b9a8-114">Remarks</span></span>

<span data-ttu-id="4b9a8-115">Crea una vista nueva en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="4b9a8-115">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="4b9a8-p101">Si el texto del comando que especifica el usuario representa un procedimiento en vez de una vista, el comportamiento dependerá del proveedor. **Se producirá un error en Append** si el proveedor no admite comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="4b9a8-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="4b9a8-118">Cuando se usa el proveedor OLE DB para Microsoft Jet, el método **Append** de la colección de **vistas** permiten especificar un **procedimiento** en lugar de una **vista** en el parámetro *Command* .</span><span class="sxs-lookup"><span data-stu-id="4b9a8-118">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="4b9a8-119">El **procedimiento** se agregará al origen de datos y a la colección **Views**.</span><span class="sxs-lookup"><span data-stu-id="4b9a8-119">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="4b9a8-120">Después del proceso **Append**, si se actualizan las colecciones **Procedures** y **Views**, el **procedimiento** ya no estará en la colección **Views** y aparecerá en la colección **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="4b9a8-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


