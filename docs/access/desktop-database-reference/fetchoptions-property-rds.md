---
title: FetchOptions (propiedad, RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3e7251ba50b003b37cdeb0dd70fe4a98821d4c9
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861936"
---
# <a name="fetchoptions-property-rds"></a><span data-ttu-id="15295-102">FetchOptions (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="15295-102">FetchOptions Property (RDS)</span></span>


<span data-ttu-id="15295-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="15295-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="15295-104">Indica el tipo de obtención asincrónica.</span><span class="sxs-lookup"><span data-stu-id="15295-104">Indicates the type of asynchronous fetching.</span></span>

## <a name="setting-and-return-values"></a><span data-ttu-id="15295-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="15295-105">Setting and Return Values</span></span>

<span data-ttu-id="15295-106">Establece o devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="15295-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15295-107">Constante</span><span class="sxs-lookup"><span data-stu-id="15295-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="15295-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="15295-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15295-109"><strong>adcFetchUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="15295-109"><strong>adcFetchUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="15295-p101">Se recuperan todos los registros del objeto <a href="recordset-object-ado.md">Recordset</a> antes de que se devuelva el control a la aplicación. El objeto completo <strong>Recordset</strong> se recupera antes de que se permita a la aplicación hacer nada con él.</span><span class="sxs-lookup"><span data-stu-id="15295-p101">All the records of the <a href="recordset-object-ado.md">Recordset</a> are fetched before control is returned to the application. The complete <strong>Recordset</strong> is fetched before the application is allowed to do anything with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15295-112"><strong>adcFetchBackground</strong></span><span class="sxs-lookup"><span data-stu-id="15295-112"><strong>adcFetchBackground</strong></span></span></p></td>
<td><p><span data-ttu-id="15295-p102">El control puede volver a la aplicación en cuanto se haya recuperado el primer lote de registros. Una posterior lectura del objeto <strong>Recordset</strong> que intente obtener acceso a un registro no recuperado en el primer lote, se retrasará hasta que se recupere realmente el registro buscado, momento en que el control volverá a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="15295-p102">Control can return to the application as soon as the first batch of records has been fetched. A subsequent read of the <strong>Recordset</strong> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15295-115"><strong>adcFetchAsync</strong></span><span class="sxs-lookup"><span data-stu-id="15295-115"><strong>adcFetchAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="15295-p103">Predeterminada. El control vuelve inmediatamente a la aplicación mientras los registros se recuperan en segundo plano. Si la aplicación intenta leer un registro que aún no se ha recuperado, se leerá el registro más cercano al buscado y el control volverá inmediatamente, lo que indica que se ha alcanzado el fin actual del objeto <strong>Recordset</strong>. Por ejemplo, una llamada a <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> moverá la posición actual del registro al último registro realmente recuperado, aunque haya más registros en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="15295-p103">Default. Control returns immediately to the application while records are fetched in the background. If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <strong>Recordset</strong> has been reached. For example, a call to <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> will move the current record position to the last record actually fetched, even though more records will continue to populate the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="15295-p104">[!NOTA] Cada archivo ejecutable del cliente que use estas constantes debe proporcionar declaraciones para ellas. Puede cortar y pegar las declaraciones de constante que desee desde el archivo Adcvbs.inc que se encuentra en la carpeta C:\Archivos de programa\Archivos comunes\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="15295-p104">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>



## <a name="remarks"></a><span data-ttu-id="15295-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15295-122">Remarks</span></span>

<span data-ttu-id="15295-123"><<<<<<< HEAD en una aplicación Web, normalmente deseará utilizar **adcFetchAsync** (el valor predeterminado), ya que proporciona un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="15295-123"><<<<<<< HEAD In a Web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance.</span></span> <span data-ttu-id="15295-124">En una aplicación cliente compilada, normalmente deseará utilizar **adcFetchBackground**.</span><span class="sxs-lookup"><span data-stu-id="15295-124">In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>
<span data-ttu-id="15295-125">=== En una aplicación web, normalmente deseará utilizar **adcFetchAsync** (el valor predeterminado), ya que proporciona un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="15295-125">======= In a web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance.</span></span> <span data-ttu-id="15295-126">En una aplicación cliente compilada, normalmente deseará utilizar **adcFetchBackground**.</span><span class="sxs-lookup"><span data-stu-id="15295-126">In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>
>>>>>>> <span data-ttu-id="15295-127">master</span><span class="sxs-lookup"><span data-stu-id="15295-127">master</span></span>

