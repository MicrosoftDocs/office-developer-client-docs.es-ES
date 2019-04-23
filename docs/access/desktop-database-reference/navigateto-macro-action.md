---
title: DesplazarseA (acción de macro)
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1c37e798e0624a5655b63a76332073e5b57c0823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288605"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="000a0-102">DesplazarseA (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="000a0-102">NavigateTo macro action</span></span>

<span data-ttu-id="000a0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="000a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="000a0-p101">Puede usar la acción **DesplazarseA** para controlar la presentación de los objetos de la base de datos en el panel de navegación. Por ejemplo, puede cambiar la manera en que los objetos de la base de datos se organizan en categorías o puede filtrar los objetos de modo que solo se muestren determinados objetos.</span><span class="sxs-lookup"><span data-stu-id="000a0-p101">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="000a0-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="000a0-106">Setting</span></span>

<span data-ttu-id="000a0-107">La acción **DesplazarseA** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="000a0-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="000a0-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="000a0-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="000a0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="000a0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="000a0-110"><strong>Categoría</strong></span><span class="sxs-lookup"><span data-stu-id="000a0-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="000a0-p102">Argumento obligatorio. Categoría por la que el panel de navegación debe mostrar los objetos. Haga clic en <strong>Tipo de objeto</strong>, <strong>Tablas y vistas</strong>, <strong>Fecha de modificación</strong>, <strong>Fecha de creación</strong>, o bien, <strong>Personalizada</strong> en el cuadro <strong>Categoría</strong>.</span><span class="sxs-lookup"><span data-stu-id="000a0-p102">Required. The category by which you want the Navigation Pane to display objects. Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="000a0-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="000a0-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="000a0-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="000a0-115">Optional.</span></span> <span data-ttu-id="000a0-116">El argumento <strong>Grupo</strong> limita los objetos que van a aparecer en el panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="000a0-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="000a0-117">Si deja en blanco el argumento <strong>Grupo</strong> , en el panel de navegación se muestran todos los objetos de la base de datos, organizados por categorías por los criterios especificados en el argumento <strong>categoría</strong> .</span><span class="sxs-lookup"><span data-stu-id="000a0-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="000a0-118">La siguiente tabla incluye ejemplos de argumentos <strong>Grupo</strong> válidos para los diversos argumentos <strong>Categoría</strong>.</span><span class="sxs-lookup"><span data-stu-id="000a0-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="000a0-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="000a0-119">Remarks</span></span>

- <span data-ttu-id="000a0-120">Esta acción es similar a seleccionar categorías y grupos en la barra de título del panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="000a0-120">This action is similar to selecting categories and groups from the title bar of the navigation pane.</span></span>

- <span data-ttu-id="000a0-p104">Los argumentos **Grupo** válidos dependen del argumento **Categoría** que se utilice. Si especifica un argumento **Grupo** no válido, aparecerá un mensaje de error.La tabla siguiente contiene ejemplo de argumentos **Grupo** válidos para cada argumento **Categoría**.</span><span class="sxs-lookup"><span data-stu-id="000a0-p104">Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p><span data-ttu-id="000a0-123">Argumento Category</span><span class="sxs-lookup"><span data-stu-id="000a0-123">Category argument</span></span></p></th>
  <th><p><span data-ttu-id="000a0-124">Ejemplo de argumentos Group</span><span class="sxs-lookup"><span data-stu-id="000a0-124">Example Group arguments</span></span></p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p><span data-ttu-id="000a0-125">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="000a0-125">Object Type</span></span></p></td>
  <td><p><span data-ttu-id="000a0-126">Tablas; Formularios; Consultas; Páginas; Macros; Módulos</span><span class="sxs-lookup"><span data-stu-id="000a0-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="000a0-127">Tablas y vistas</span><span class="sxs-lookup"><span data-stu-id="000a0-127">Tables and Views</span></span></p></td>
  <td><p><span data-ttu-id="000a0-128">Nombres de tablas específicas de la base de datos</span><span class="sxs-lookup"><span data-stu-id="000a0-128">Names of specific tables in your database</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="000a0-129">Fecha de modificación</span><span class="sxs-lookup"><span data-stu-id="000a0-129">Modified Date</span></span></p></td>
  <td><p><span data-ttu-id="000a0-130">Hoy; Ayer; Mes pasado; Con más de</span><span class="sxs-lookup"><span data-stu-id="000a0-130">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="000a0-131">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="000a0-131">Created Date</span></span></p></td>
  <td><p><span data-ttu-id="000a0-132">Hoy; Ayer; El mes pasado; Antiguo</span><span class="sxs-lookup"><span data-stu-id="000a0-132">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="000a0-133">Categoría personalizada</span><span class="sxs-lookup"><span data-stu-id="000a0-133">Custom category</span></span></p></td>
  <td><p><span data-ttu-id="000a0-134">Nombres de grupos que creó para la categoría personalizada especificada</span><span class="sxs-lookup"><span data-stu-id="000a0-134">Names of groups you have created for the specified custom category</span></span></p></td>
  </tr>
  </tbody>
  </table>

- <span data-ttu-id="000a0-135">Para ejecutar la acción **DesplazarseA** en un módulo de VBA, use el método **NavigateTo** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="000a0-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>

> [!NOTE]
> <span data-ttu-id="000a0-p105">[!NOTA] Para desplazarse al nivel superior de una categoría (por ejemplo, **Todas las tablas**, **Todos los objetos de Access** o **Todas las fechas**), deje el argumento Grupo en blanco. Por ejemplo, cuando el valor del argumento **Categoría** es **Tipo de objeto** y se especifica **Todos los objetos de Access** como argumento **Grupo**, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="000a0-p105">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank. For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span></span>


