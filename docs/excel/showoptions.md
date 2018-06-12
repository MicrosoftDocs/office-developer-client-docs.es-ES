---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815699"
---
# <a name="showoptions"></a><span data-ttu-id="b9697-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="b9697-103">ShowOptions</span></span>

<span data-ttu-id="b9697-104">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b9697-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b9697-105">Muestra un cuadro de diálogo modal para recopilar información del usuario.</span><span class="sxs-lookup"><span data-stu-id="b9697-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="b9697-106">En este punto de entrada se llama cuando un usuario hace clic en el botón de **Opciones** situada junto al cuadro **tipo de clúster** para el conector de clúster seleccionado en el cuadro de diálogo **Opciones de Excel** (en la categoría **Avanzadas** , en la sección **fórmulas** ).</span><span class="sxs-lookup"><span data-stu-id="b9697-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="b9697-107">Conectores de clúster son responsables para implementar su propia interfaz de cuadro de diálogo Opciones y para almacenar los datos relacionados en el registro o en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="b9697-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="b9697-108">Las opciones son internas para el conector de clúster.</span><span class="sxs-lookup"><span data-stu-id="b9697-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="b9697-109">Excel no es consciente de ellos.</span><span class="sxs-lookup"><span data-stu-id="b9697-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="b9697-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9697-110">Parameters</span></span>

<span data-ttu-id="b9697-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="b9697-111">_hWndParent_</span></span>
  
> <span data-ttu-id="b9697-112">Identificador de la ventana de Excel.</span><span class="sxs-lookup"><span data-stu-id="b9697-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b9697-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9697-113">Return value</span></span>

<span data-ttu-id="b9697-114">**xlHpcRetSuccess** si se muestra el cuadro de diálogo; **xlHpcRetCallFailed** si no se muestra.</span><span class="sxs-lookup"><span data-stu-id="b9697-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b9697-115">Notas</span><span class="sxs-lookup"><span data-stu-id="b9697-115">Remarks</span></span>

<span data-ttu-id="b9697-116">Conectores de clúster pueden usar este cuadro de diálogo para obtener información, por ejemplo, qué servidor de clúster se usa, desde el usuario.</span><span class="sxs-lookup"><span data-stu-id="b9697-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9697-117">Ver también</span><span class="sxs-lookup"><span data-stu-id="b9697-117">See also</span></span>

- [<span data-ttu-id="b9697-118">Funciones de conector de clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="b9697-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

