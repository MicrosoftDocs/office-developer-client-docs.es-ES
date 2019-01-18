---
title: Acción de macro Beep (referencia de escritorio de la base de datos de Access)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721475"
---
# <a name="beep-macro-action"></a><span data-ttu-id="88ae4-102">Bip (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="88ae4-102">Beep macro action</span></span>


<span data-ttu-id="88ae4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88ae4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88ae4-104">La acción **Bip** se puede utilizar para emitir un sonido a través de los altavoces del equipo.</span><span class="sxs-lookup"><span data-stu-id="88ae4-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="88ae4-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="88ae4-105">Setting</span></span>

<span data-ttu-id="88ae4-106">La acción **Bip** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="88ae4-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ae4-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88ae4-107">Remarks</span></span>

<span data-ttu-id="88ae4-108">La acción **Bip** se puede utilizar para indicar las circunstancias siguientes:</span><span class="sxs-lookup"><span data-stu-id="88ae4-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="88ae4-109">Se produjeron cambios importantes en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="88ae4-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="88ae4-p101">Se han especificado datos de un tipo incorrecto en un control. Por ejemplo, si el usuario ha especificado datos numéricos en un control de cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="88ae4-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="88ae4-112">Una macro ha llegado a un punto específico o ha finalizado sus acciones.</span><span class="sxs-lookup"><span data-stu-id="88ae4-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="88ae4-113">La frecuencia y la duración del tono dependen del hardware, que puede ser diferente en cada equipo.</span><span class="sxs-lookup"><span data-stu-id="88ae4-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="88ae4-114">Para ejecutar la acción **Bip** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Beep** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="88ae4-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

