---
title: CerrarBaseDeDatos (acción de macro)
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2c60d53b6798d3385bdcfb17669134a04ba6195
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486652"
---
# <a name="closedatabase-macro-action"></a><span data-ttu-id="2d75f-102">CerrarBaseDeDatos (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="2d75f-102">CloseDatabase Macro Action</span></span>


<span data-ttu-id="2d75f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d75f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d75f-104">La acción **CerrarBaseDeDatos** puede usarse para cerrar la actual base de datos.</span><span class="sxs-lookup"><span data-stu-id="2d75f-104">You can use the **CloseDatabase** action to close the current database.</span></span>

## <a name="setting"></a><span data-ttu-id="2d75f-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="2d75f-105">Setting</span></span>

<span data-ttu-id="2d75f-106">La acción **CerrarBaseDeDatos** no tiene ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="2d75f-106">The **CloseDatabase** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d75f-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d75f-107">Remarks</span></span>

  - <span data-ttu-id="2d75f-108">Access no ejecuta ninguna acción que siga a la acción **CerrarBaseDeDatos** de una macro.</span><span class="sxs-lookup"><span data-stu-id="2d75f-108">Access will not run any actions that follow the **CloseDatabase** action in a macro.</span></span>

  - <span data-ttu-id="2d75f-109">Esta acción tiene el mismo efecto que hacer clic en la pestaña **archivo** y, a continuación, haciendo clic en **Cerrar base de datos**.</span><span class="sxs-lookup"><span data-stu-id="2d75f-109">This action has the same effect as clicking the **File** tab and then clicking **Close Database**.</span></span> <span data-ttu-id="2d75f-110">Si hay objetos abiertos que no se guardaron cuando ejecuta la acción **CerrarBaseDeDatos**, los cuadros de diálogo que aparecen son los mismos que los que se muestran al hacer clic en **Cerrar base de datos**.</span><span class="sxs-lookup"><span data-stu-id="2d75f-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span></span>

  - <span data-ttu-id="2d75f-111">Para ejecutar la acción **CerrarBaseDeDatos** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **CloseDatabase** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="2d75f-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span></span>

