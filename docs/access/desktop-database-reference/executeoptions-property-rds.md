---
title: ExecuteOptions (propiedad, RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6db51927182008314da045021f81e6547d5d78be
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026144"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="11401-102">ExecuteOptions (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="11401-102">ExecuteOptions property (RDS)</span></span>


<span data-ttu-id="11401-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11401-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11401-104">Indica si la ejecución asincrónica está habilitada.</span><span class="sxs-lookup"><span data-stu-id="11401-104">Indicates whether asynchronous execution is enabled.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="11401-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="11401-105">Settings and return values</span></span>

<span data-ttu-id="11401-106">Establece o devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="11401-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11401-107">Constante</span><span class="sxs-lookup"><span data-stu-id="11401-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="11401-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="11401-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11401-109"><strong>adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="11401-109"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="11401-110">Ejecuta la siguiente actualización del objeto <a href="recordset-object-ado.md">Recordset</a> de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="11401-110">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11401-111"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="11401-111"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="11401-p101">Predeterminada. Ejecuta la siguiente actualización del objeto <strong>Recordset</strong> de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="11401-p101">Default. Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="11401-p102">[!NOTA] Cada archivo ejecutable del cliente que usa estas constantes debe proporcionar declaraciones. Puede cortar y pegar las declaraciones de constante que desee desde el archivo Adcvbs.inc que se encuentra en la carpeta C:\Archivos de programa\Archivos comunes\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="11401-p102">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="11401-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11401-116">Remarks</span></span>

<span data-ttu-id="11401-117">Si **ExecuteOptions** está establecida en **adcExecAsync**, ejecuta de forma asincrónica la siguiente llamada **Refresh** en el objeto [Recordset](datacontrol-object-rds.md) de **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="11401-117">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="11401-118">Si intenta llamar a [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) o [Recordset](recordset-sourcerecordset-properties-rds.md) mientras se ejecuta otra operación asincrónica que podría cambiar el objeto [Recordset](datacontrol-object-rds.md) de **RDS.DataControl**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="11401-118">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="11401-119">Si se produce un error durante una operación asincrónica, el valor [ReadyState](readystate-property-rds.md) del objeto **RDS.DataControl** cambia de **adcReadyStateLoaded** a **adcReadyStateComplete** y el valor de la propiedad **Recordset** sigue siendo *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="11401-119">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

