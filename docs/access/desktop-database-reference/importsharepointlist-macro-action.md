---
title: ImportarListaDeSharePoint (acción de macro)
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291862"
---
# <a name="importsharepointlist-macro-action"></a><span data-ttu-id="ec782-102">ImportarListaDeSharePoint (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="ec782-102">ImportSharePointList macro action</span></span>

<span data-ttu-id="ec782-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec782-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec782-104">Puede usar la acción **ImportarListaDeSharePoint** para importar o vincular los datos de un sitio de Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="ec782-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span></span>

> [!NOTE]
> <span data-ttu-id="ec782-105">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="ec782-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="ec782-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="ec782-106">Setting</span></span>

<span data-ttu-id="ec782-107">La acción **ImportarListaDeSharePoint** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="ec782-107">The **ImportSharePointList** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec782-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="ec782-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ec782-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec782-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec782-110"><strong>Tipo de transferencia</strong></span><span class="sxs-lookup"><span data-stu-id="ec782-110"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="ec782-111">Seleccione el tipo de transferencia.</span><span class="sxs-lookup"><span data-stu-id="ec782-111">Select the type of transfer.</span></span></p>
<ul>
<li><p><span data-ttu-id="ec782-112">Seleccione <strong>importar</strong> para copiar los datos de SharePoint Foundation en una tabla de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ec782-112">Select <strong>Import</strong> to copy the SharePoint Foundation data into a table in Microsoft Access.</span></span> <span data-ttu-id="ec782-113">Las actualizaciones de los datos en Access no afectan a los datos de SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="ec782-113">Updates to the data in Access do not affect the data in SharePoint Foundation.</span></span> <span data-ttu-id="ec782-114">Del mismo modo, las actualizaciones de los datos en SharePoint Foundation no afectan a los datos de Access.</span><span class="sxs-lookup"><span data-stu-id="ec782-114">Likewise, updates to the data in SharePoint Foundation do not affect the data in Access.</span></span></p></li>
<li><p><span data-ttu-id="ec782-115">Seleccione <strong>vincular</strong> para crear una tabla vinculada en Access que se vincule a los datos en SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="ec782-115">Select <strong>Link</strong> to create a linked table in Access that links to the data in SharePoint Foundation.</span></span> <span data-ttu-id="ec782-116">Las actualizaciones de los datos en Access se reflejan en SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="ec782-116">Updates to the data in Access are reflected in SharePoint Foundation.</span></span> <span data-ttu-id="ec782-117">Del mismo modo, las actualizaciones de los datos en SharePoint Foundation se reflejan en Access.</span><span class="sxs-lookup"><span data-stu-id="ec782-117">Likewise, updates to the data in SharePoint Foundation are reflected in Access.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec782-118"><strong>Dirección del sitio</strong></span><span class="sxs-lookup"><span data-stu-id="ec782-118"><strong>Site Address</strong></span></span></p></td>
<td><p><span data-ttu-id="ec782-119">Escriba la ruta de acceso completa al sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ec782-119">Enter the full path of the SharePoint site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec782-120"><strong>Id. de lista</strong></span><span class="sxs-lookup"><span data-stu-id="ec782-120"><strong>List ID</strong></span></span></p></td>
<td><p><span data-ttu-id="ec782-p103">Escriba el nombre o el identificador GUID de la lista que se va a transferir. Es un argumento obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ec782-p103">Enter the name or GUID of the list to be transferred. Required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec782-123"><strong>Id. de vista</strong></span><span class="sxs-lookup"><span data-stu-id="ec782-123"><strong>View ID</strong></span></span></p></td>
<td><p><span data-ttu-id="ec782-p104">Escriba el identificador GUID de la vista de la lista que desee usar. Deje este argumento en blanco para transferir todas las filas y columnas de la lista.</span><span class="sxs-lookup"><span data-stu-id="ec782-p104">Enter the GUID of the view for the list you want to use. Leave this argument blank to transfer all rows and columns in the list.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec782-126"><strong>Nombre de la tabla</strong></span><span class="sxs-lookup"><span data-stu-id="ec782-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ec782-127">Especifique el nombre que desee mostrar para la tabla o la tabla vinculada en Access.</span><span class="sxs-lookup"><span data-stu-id="ec782-127">Enter the name you want displayed for the table or linked table in Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec782-128"><strong>Obtener valores de presentación de búsqueda</strong></span><span class="sxs-lookup"><span data-stu-id="ec782-128"><strong>Get Lookup Display Values</strong></span></span></p></td>
<td><p><span data-ttu-id="ec782-129">Seleccione <strong>Sí</strong> para transferir los valores de presentación de los campos de búsqueda en vez del identificador usado para llevar a cabo la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ec782-129">Select <strong>Yes</strong> to transfer display values for Lookup fields instead of the ID used to perform the lookup.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ec782-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec782-130">Remarks</span></span>

- <span data-ttu-id="ec782-131">Esta acción es lo mismo que hacer clic en **Lista de SharePoint** del grupo **Importar** en la ficha **Datos externos**. Los argumentos de la acción se corresponden con las opciones seleccionadas en el Asistente para obtener valores externos.</span><span class="sxs-lookup"><span data-stu-id="ec782-131">This action has the same effect as clicking **SharePoint List** in the **Import** group on the **External Data** tab. The arguments for the action correspond to the choices you make in the Get External Data Wizard.</span></span>

- <span data-ttu-id="ec782-132">Para ejecutar la acción **ImportarListaDeSharePoint** en un módulo de VBA, use el método **TransferSharePointList** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="ec782-132">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="ec782-133">Si especifica una lista o una vista inexistentes, no se producirán errores ni se transferirá ningún dato.</span><span class="sxs-lookup"><span data-stu-id="ec782-133">If you specify a nonexistent list or view, no error occurs, and no data is transferred.</span></span>

- <span data-ttu-id="ec782-p105">Un identificador GUID es un identificador hexadecimal único de una lista o una vista. Dicho identificador debe especificarse en el formato siguiente, donde cada "F" es un número hexadecimal (del 0 al 9 o de la A a la F).</span><span class="sxs-lookup"><span data-stu-id="ec782-p105">A GUID is a unique hexadecimal identifier for a list or a view. A GUID must be entered in the following format, where each "F" is a hexadecimal number (0 through 9 or A through F).</span></span>
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  <span data-ttu-id="ec782-136">Para obtener el identificador GUID de una lista o una vista del sitio de SharePoint puede utilizar el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="ec782-136">You can obtain the GUID for a list or view from the SharePoint site by using the following procedure:</span></span>
    
  1. <span data-ttu-id="ec782-137">Abra la lista de SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="ec782-137">Open the list in SharePoint Foundation.</span></span>
    
  2. <span data-ttu-id="ec782-138">Si no se muestra la vista que desea, haga clic en la flecha desplegable **Ver** y, a continuación, seleccione la vista deseada.</span><span class="sxs-lookup"><span data-stu-id="ec782-138">If the view you want is not displayed, click the **View** drop-down arrow and then select the view you want.</span></span>
    
  3. <span data-ttu-id="ec782-139">Haga clic en la flecha desplegable **Ver** y, a continuación, seleccione **Modificar esta vista**.La dirección de la barra de dirección del explorador contiene los identificadores tanto de la lista como de la vista.</span><span class="sxs-lookup"><span data-stu-id="ec782-139">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span></span> <span data-ttu-id="ec782-140">El identificador GUID de la lista sigue a **List=**, y el de la vista sigue a **View=**.</span><span class="sxs-lookup"><span data-stu-id="ec782-140">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span></span> <span data-ttu-id="ec782-141">Sin embargo, en la dirección, cada carácter **{** (abrir llave) se representa mediante la cadena **%7B**, cada carácter **-** (guión) mediante la cadena **%2D**, y cada carácter **}** (cerrar llave) mediante la cadena **%7D**.</span><span class="sxs-lookup"><span data-stu-id="ec782-141">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span></span> <span data-ttu-id="ec782-142">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ec782-142">For example:</span></span>
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  <span data-ttu-id="ec782-143">Antes de poder usar los GUID de la dirección como argumentos en esta acción de macro, debe reemplazar cada cadena **% 7B** con el carácter **{** , reemplazar cada cadena **2D%** por el **-** carácter y reemplazar cada cadena **% 7D** por el **}** carácter.</span><span class="sxs-lookup"><span data-stu-id="ec782-143">Before you can use the GUIDs from the address as arguments in this macro action, you must replace each **%7B** string with the **{** character, replace each **%2D** string with the **-** character, and replace each **%7D** string with the **}** character.</span></span> <span data-ttu-id="ec782-144">No incluya el carácter **&** (y comercial) que sigue a la cadena **%7D** en el identificador GUID de la lista.</span><span class="sxs-lookup"><span data-stu-id="ec782-144">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span></span>

