---
title: OPENFILE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Abre un documento Visio microsoft, si aún no está abierto, y activa la ventana del documento.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419579"
---
# <a name="openfile-function"></a><span data-ttu-id="1001a-103">Función OPENFILE</span><span class="sxs-lookup"><span data-stu-id="1001a-103">OPENFILE Function</span></span>

<span data-ttu-id="1001a-104">Abre un documento Visio microsoft, si aún no está abierto, y activa la ventana del documento.</span><span class="sxs-lookup"><span data-stu-id="1001a-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1001a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1001a-105">Syntax</span></span>

 <span data-ttu-id="1001a-106">**OPENFILE**( _"filename"_)</span><span class="sxs-lookup"><span data-stu-id="1001a-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="1001a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1001a-107">Parameters</span></span>

|<span data-ttu-id="1001a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1001a-108">**Name**</span></span>|<span data-ttu-id="1001a-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1001a-109">**Required/Optional**</span></span>|<span data-ttu-id="1001a-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="1001a-110">**Data Type**</span></span>|<span data-ttu-id="1001a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1001a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1001a-112">_filename_</span><span class="sxs-lookup"><span data-stu-id="1001a-112">_filename_</span></span> <br/> |<span data-ttu-id="1001a-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1001a-113">Required</span></span>  <br/> |<span data-ttu-id="1001a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1001a-114">**String**</span></span> <br/> |<span data-ttu-id="1001a-115">Nombre del archivo, incluida la ruta de acceso de archivo, que desea abrir.</span><span class="sxs-lookup"><span data-stu-id="1001a-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1001a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1001a-116">Remarks</span></span>

<span data-ttu-id="1001a-p101">Si hay varias llamadas a la función OPENFILE, se van agregando a una cola y se ejecutan en el orden en que se hayan ido evaluando. Si el documento actual de Visio está activado para modificarlo visualmente, se iniciará una copia nueva de Visio con el nombre de archivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="1001a-p101">Multiple OPENFILE function calls are queued and executed in order of evaluation. If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="1001a-119">Esta función siempre devuelve el valor FALSE.</span><span class="sxs-lookup"><span data-stu-id="1001a-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="1001a-p102">En versiones anteriores de la aplicación Visio, esta función se denominaba _OPENFILE. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones.</span><span class="sxs-lookup"><span data-stu-id="1001a-p102">In earlier versions of the Visio application, this function appears as _OPENFILE. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1001a-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1001a-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="1001a-123">Abre el archivo especificado "MyFile.vsdx" en una nueva ventana o activa la ventana si el archivo ya está abierto.</span><span class="sxs-lookup"><span data-stu-id="1001a-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

