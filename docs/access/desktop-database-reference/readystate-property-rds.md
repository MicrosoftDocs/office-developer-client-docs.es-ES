---
title: ReadyState (propiedad, RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 71dd674e90e2438c616f0973c4f9948f1b20b1f1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714783"
---
# <a name="readystate-property-rds"></a><span data-ttu-id="7e3a5-102">ReadyState (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="7e3a5-102">ReadyState property (RDS)</span></span>

<span data-ttu-id="7e3a5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e3a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e3a5-104">Indica el progreso de un objeto [DataControl](datacontrol-object-rds.md) a medida que recupera datos en su objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7e3a5-104">Indicates the progress of a [DataControl](datacontrol-object-rds.md) object as it retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7e3a5-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="7e3a5-105">Settings and return values</span></span>

<span data-ttu-id="7e3a5-106">Establece o devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7e3a5-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e3a5-107">Valor</span><span class="sxs-lookup"><span data-stu-id="7e3a5-107">Value</span></span></p></th>
<th><p><span data-ttu-id="7e3a5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e3a5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e3a5-109"><strong>adcReadyStateLoaded</strong></span><span class="sxs-lookup"><span data-stu-id="7e3a5-109"><strong>adcReadyStateLoaded</strong></span></span></p></td>
<td><p><span data-ttu-id="7e3a5-p101">La consulta actual se sigue ejecutando y no se ha recuperado ninguna fila. El objeto <strong>Recordset</strong> de <strong>DataControl</strong> no está disponible para ser usado.</span><span class="sxs-lookup"><span data-stu-id="7e3a5-p101">The current query is still executing and no rows have been fetched. The <strong>DataControl</strong> object's <strong>Recordset</strong> is not available for use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3a5-112"><strong>adcReadyStateInteractive</strong></span><span class="sxs-lookup"><span data-stu-id="7e3a5-112"><strong>adcReadyStateInteractive</strong></span></span></p></td>
<td><p><span data-ttu-id="7e3a5-p102">Un conjunto inicial de filas recuperadas por la consulta actual se almacenó en el objeto <strong>Recordset</strong> de <strong>DataControl</strong> y está disponible para ser usado. Las filas restantes se están recuperando.</span><span class="sxs-lookup"><span data-stu-id="7e3a5-p102">An initial set of rows retrieved by the current query has been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use. The remaining rows are still being fetched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3a5-115"><strong>adcReadyStateComplete</strong></span><span class="sxs-lookup"><span data-stu-id="7e3a5-115"><strong>adcReadyStateComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="7e3a5-116">Todas las filas recuperadas por la consulta actual han sido almacenadas en el objeto <strong>Recordset</strong> de <strong>DataControl</strong> y están disponibles para ser usadas.
</span><span class="sxs-lookup"><span data-stu-id="7e3a5-116">All rows retrieved by the current query have been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="7e3a5-117">Este estado también existirá si se anuló una operación a causa de un error o si no se inicializó el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e3a5-117">This state will also exist if an operation aborted due to an error, or if the <strong>Recordset</strong> object is not initialized.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7e3a5-p104">[!NOTA] Cada archivo ejecutable del cliente que use estas constantes debe proporcionar declaraciones para ellas. Puede cortar y pegar las declaraciones de constante que desee desde el archivo Adcvbs.inc que se encuentra en la carpeta C:\Archivos de programa\Archivos comunes\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="7e3a5-p104">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e3a5-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e3a5-120">Remarks</span></span>

<span data-ttu-id="7e3a5-p105">Utilice el evento [onReadyStateChange](onreadystatechange-event-rds.md) para controlar los cambios realizados en la propiedad **ReadyState** durante una operación de consulta asincrónica. Eso es más eficaz que comprobar de forma periódica el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7e3a5-p105">Use the [onReadyStateChange](onreadystatechange-event-rds.md) event to monitor changes in the **ReadyState** property during an asynchronous query operation. This is more efficient than periodically checking the value of the property.</span></span>

<span data-ttu-id="7e3a5-123">Si se produce un error durante una operación asincrónica, la propiedad **ReadyState** cambia a **adcReadyStateComplete**, la propiedad [State](state-property-ado.md) cambia de **adStateExecuting** a **adStateClosed**y el **conjunto de registros** propiedad [Value](value-property-ado.md) del objeto permanece como *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="7e3a5-123">If an error occurs during an asynchronous operation, the **ReadyState** property changes to **adcReadyStateComplete**, the [State](state-property-ado.md) property changes from **adStateExecuting** to **adStateClosed**, and the **Recordset** object [Value](value-property-ado.md) property remains *Nothing*.</span></span>

