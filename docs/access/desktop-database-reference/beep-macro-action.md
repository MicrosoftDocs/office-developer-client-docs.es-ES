---
title: Acción de Macro Beep (referencia de escritorio de la base de datos de Access)
TOCTitle: Beep Macro Action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7024734b09544042fa58b8cd95127d8195e5788a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486127"
---
# <a name="beep-macro-action"></a><span data-ttu-id="88396-102">Bip (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="88396-102">Beep Macro Action</span></span>


<span data-ttu-id="88396-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="88396-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="88396-104">La acción **Bip** se puede utilizar para emitir un sonido a través de los altavoces del equipo.</span><span class="sxs-lookup"><span data-stu-id="88396-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="88396-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="88396-105">Setting</span></span>

<span data-ttu-id="88396-106">La acción **Bip** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="88396-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="88396-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88396-107">Remarks</span></span>

<span data-ttu-id="88396-108">La acción **Bip** se puede utilizar para indicar las circunstancias siguientes:</span><span class="sxs-lookup"><span data-stu-id="88396-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="88396-109">Se produjeron cambios importantes en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="88396-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="88396-p101">Se han especificado datos de un tipo incorrecto en un control. Por ejemplo, si el usuario ha especificado datos numéricos en un control de cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="88396-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="88396-112">Una macro ha llegado a un punto específico o ha finalizado sus acciones.</span><span class="sxs-lookup"><span data-stu-id="88396-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="88396-113">La frecuencia y la duración del tono dependen del hardware, que puede ser diferente en cada equipo.</span><span class="sxs-lookup"><span data-stu-id="88396-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="88396-114">Para ejecutar la acción **Bip** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Beep** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="88396-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

