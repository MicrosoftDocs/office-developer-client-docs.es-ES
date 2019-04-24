---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310430"
---
# <a name="showoptions"></a><span data-ttu-id="a5348-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="a5348-103">ShowOptions</span></span>

<span data-ttu-id="a5348-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5348-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a5348-105">Muestra un cuadro de diálogo modal para recopilar información del usuario.</span><span class="sxs-lookup"><span data-stu-id="a5348-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="a5348-106">Se llama a este punto de entrada cuando un usuario hace clic en el botón **Opciones** situado junto al cuadro **tipo de clúster** para el conector de clúster seleccionado en el cuadro de diálogo **Opciones de Excel** (en la categoría **avanzadas** , en la sección **fórmulas** ).</span><span class="sxs-lookup"><span data-stu-id="a5348-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="a5348-107">Los conectores de clúster son responsables de implementar su propia interfaz de diálogo de opciones y de almacenar los datos relacionados en el registro o en cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="a5348-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="a5348-108">Las opciones son internas al conector del clúster.</span><span class="sxs-lookup"><span data-stu-id="a5348-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="a5348-109">Excel no es consciente de ellos.</span><span class="sxs-lookup"><span data-stu-id="a5348-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="a5348-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="a5348-110">Parameters</span></span>

<span data-ttu-id="a5348-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="a5348-111">_hWndParent_</span></span>
  
> <span data-ttu-id="a5348-112">Identificador de la ventana de Excel.</span><span class="sxs-lookup"><span data-stu-id="a5348-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5348-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5348-113">Return value</span></span>

<span data-ttu-id="a5348-114">**xlHpcRetSuccess** si se mostró el cuadro de diálogo; **xlHpcRetCallFailed** si no se mostró.</span><span class="sxs-lookup"><span data-stu-id="a5348-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a5348-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5348-115">Remarks</span></span>

<span data-ttu-id="a5348-116">Los conectores de clúster pueden usar este cuadro de diálogo para obtener información, como el servidor de clúster que se va a usar, del usuario.</span><span class="sxs-lookup"><span data-stu-id="a5348-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5348-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5348-117">See also</span></span>

- [<span data-ttu-id="a5348-118">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="a5348-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

