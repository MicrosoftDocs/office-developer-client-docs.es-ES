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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407700"
---
# <a name="showoptions"></a><span data-ttu-id="2048b-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="2048b-103">ShowOptions</span></span>

<span data-ttu-id="2048b-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2048b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2048b-105">Muestra un cuadro de diálogo modal para recopilar información del usuario.</span><span class="sxs-lookup"><span data-stu-id="2048b-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="2048b-106">Este punto de entrada se llama  cuando un  usuario hace clic en el botón Opciones situado junto al  cuadro Tipo de clúster del conector de clúster seleccionado en el cuadro de diálogo Opciones de **Excel** (en la categoría Avanzadas de la sección **Fórmulas).**</span><span class="sxs-lookup"><span data-stu-id="2048b-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="2048b-107">Los conectores de clúster son responsables de implementar su propia interfaz de diálogo de opciones y de almacenar los datos relacionados en el Registro o en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="2048b-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="2048b-108">Las opciones son internas del conector de clúster.</span><span class="sxs-lookup"><span data-stu-id="2048b-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="2048b-109">Excel no es consciente de ellos.</span><span class="sxs-lookup"><span data-stu-id="2048b-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="2048b-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="2048b-110">Parameters</span></span>

<span data-ttu-id="2048b-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="2048b-111">_hWndParent_</span></span>
  
> <span data-ttu-id="2048b-112">Un identificador de la Excel ventana.</span><span class="sxs-lookup"><span data-stu-id="2048b-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2048b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2048b-113">Return value</span></span>

<span data-ttu-id="2048b-114">**xlHpcRetSuccess** si se mostró el cuadro de diálogo; **xlHpcRetCallFailed** si no se mostró.</span><span class="sxs-lookup"><span data-stu-id="2048b-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2048b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2048b-115">Remarks</span></span>

<span data-ttu-id="2048b-116">Los conectores de clúster pueden usar este cuadro de diálogo para obtener información, como el servidor de clúster que se va a usar, del usuario.</span><span class="sxs-lookup"><span data-stu-id="2048b-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2048b-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="2048b-117">See also</span></span>

- [<span data-ttu-id="2048b-118">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="2048b-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

