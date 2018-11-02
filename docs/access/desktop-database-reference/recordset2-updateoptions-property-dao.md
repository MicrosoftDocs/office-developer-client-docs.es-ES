---
title: Propiedad Recordset2.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ad1428d9a820a2489a9051ca77c0de854e03d57
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920854"
---
# <a name="recordset2updateoptions-property-dao"></a><span data-ttu-id="e006c-102">Propiedad Recordset2.UpdateOptions (DAO)</span><span class="sxs-lookup"><span data-stu-id="e006c-102">Recordset2.UpdateOptions property (DAO)</span></span>


<span data-ttu-id="e006c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e006c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="e006c-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e006c-104">Syntax</span></span>

<span data-ttu-id="e006c-105">*expresión* . UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="e006c-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="e006c-106">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="e006c-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e006c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e006c-107">Remarks</span></span>

<span data-ttu-id="e006c-108">Cuando se ejecuta **[Update](recordset2-update-method-dao.md)** en modo por lotes, DAO y la biblioteca de cursores por lotes cliente crean una serie de instrucciones SQL UPDATE para realizar los cambios necesarios.</span><span class="sxs-lookup"><span data-stu-id="e006c-108">When a batch-mode **[Update](recordset2-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="e006c-109">Se crea una cláusula SQL WHERE para cada actualización para aislar los registros marcados como modificados por la propiedad **[RecordStatus](recordset2-recordstatus-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e006c-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset2-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="e006c-110">Como algunos servidores remotos usan desencadenadores u otras formas para aplicar la integridad referencial, con frecuencia es importante limitar la actualización de los campos solo a los afectados por el cambio.</span><span class="sxs-lookup"><span data-stu-id="e006c-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="e006c-111">Para ello, establezca la propiedad **UpdateOptions** en una de las siguientes constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** o **dbCriteriaTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="e006c-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="e006c-112">De esta forma, solo se ejecuta la cantidad mínima total de código desencadenador.</span><span class="sxs-lookup"><span data-stu-id="e006c-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="e006c-113">Como resultado, la operación de actualización se ejecuta con más rapidez y con menos errores potenciales.</span><span class="sxs-lookup"><span data-stu-id="e006c-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="e006c-p103">También puede concatenar cualquiera de las constantes **dbCriteriaDeleteInsert** o **dbCriteriaUpdate** para determinar si debe utilizar un conjunto de instrucciones SQL DELETE e INSERT o una instrucción SQL UPDATE para cada actualización cuando se devuelven modificaciones por lotes al servidor. En el primer caso, se requieren dos operaciones distintas para actualizar el registro. En algunos casos, sobre todo cuando el sistema remoto implementa los desencadenadores DELETE, INSERT y UPDATE, al elegir el valor correcto de la propiedad **UpdateOptions** se puede afectar significativamente en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e006c-p103">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server. In the former case, two separate operations are required to update the record. In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="e006c-117">Si no especifica ninguna de las constantes, se utilizarán **dbCriteriaUpdate** y **dbCriteriaKey**.</span><span class="sxs-lookup"><span data-stu-id="e006c-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="e006c-118">Los últimos registros agregados generarán siempre instrucciones INSERT y los elementos eliminados generarán instrucciones DELETE, por ello esta propiedad sólo se aplica según se modificaron los registros con las actualizaciones de las bibliotecas de cursores.</span><span class="sxs-lookup"><span data-stu-id="e006c-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

