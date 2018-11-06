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
ms.openlocfilehash: 7da3eb87e775a6b02694910cd017c9535fde1df7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998283"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="42dc4-102">DesplazarseA (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="42dc4-102">NavigateTo macro action</span></span>

<span data-ttu-id="42dc4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42dc4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42dc4-p101">Puede usar la acción **DesplazarseA** para controlar la presentación de los objetos de la base de datos en el panel de navegación. Por ejemplo, puede cambiar la manera en que los objetos de la base de datos se organizan en categorías o puede filtrar los objetos de modo que solo se muestren determinados objetos.</span><span class="sxs-lookup"><span data-stu-id="42dc4-p101">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="42dc4-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="42dc4-106">Setting</span></span>

<span data-ttu-id="42dc4-107">La acción **DesplazarseA** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="42dc4-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42dc4-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="42dc4-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="42dc4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="42dc4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42dc4-110"><strong>Categor?a</strong></span><span class="sxs-lookup"><span data-stu-id="42dc4-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="42dc4-p102">Argumento obligatorio. Categoría por la que el panel de navegación debe mostrar los objetos. Haga clic en <strong>Tipo de objeto</strong>, <strong>Tablas y vistas</strong>, <strong>Fecha de modificación</strong>, <strong>Fecha de creación</strong>, o bien, <strong>Personalizada</strong> en el cuadro <strong>Categoría</strong>.</span><span class="sxs-lookup"><span data-stu-id="42dc4-p102">Required. The category by which you want the Navigation Pane to display objects. Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42dc4-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="42dc4-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="42dc4-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="42dc4-115">Optional.</span></span> <span data-ttu-id="42dc4-116">El argumento <strong>grupo</strong> limita los objetos en la categoría que aparece en el panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="42dc4-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="42dc4-117">Si deja en blanco el argumento <strong>grupo</strong> , el panel de navegación muestra todos los objetos de base de datos, clasificados por los criterios especificados en el argumento <strong>categoría</strong> .</span><span class="sxs-lookup"><span data-stu-id="42dc4-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="42dc4-118">En la tabla siguiente se muestran ejemplos de argumentos  <strong>Group</strong> válidos para los distintos argumentos <strong>Category</strong>.</span><span class="sxs-lookup"><span data-stu-id="42dc4-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="42dc4-119">Notas</span><span class="sxs-lookup"><span data-stu-id="42dc4-119">Remarks</span></span>

- <span data-ttu-id="42dc4-120">Esta acción es similar a seleccionar categorías y grupos de la barra de título del panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="42dc4-120">This action is similar to selecting categories and groups from the title bar of the navigation pane.</span></span>

- <span data-ttu-id="42dc4-p104">Los argumentos **Grupo** válidos dependen del argumento **Categoría** que se utilice. Si especifica un argumento **Grupo** no válido, aparecerá un mensaje de error.La tabla siguiente contiene ejemplo de argumentos **Grupo** válidos para cada argumento **Categoría**.</span><span class="sxs-lookup"><span data-stu-id="42dc4-p104">Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p><span data-ttu-id="42dc4-123">Argumento Categoría</span><span class="sxs-lookup"><span data-stu-id="42dc4-123">Category argument</span></span></p></th>
  <th><p><span data-ttu-id="42dc4-124">Ejemplo de argumentos Grupo</span><span class="sxs-lookup"><span data-stu-id="42dc4-124">Example Group arguments</span></span></p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p><span data-ttu-id="42dc4-125">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="42dc4-125">Object Type</span></span></p></td>
  <td><p><span data-ttu-id="42dc4-126">Tablas; Formularios; Consultas; Páginas; Macros; Módulos</span><span class="sxs-lookup"><span data-stu-id="42dc4-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="42dc4-127">Tablas y vistas</span><span class="sxs-lookup"><span data-stu-id="42dc4-127">Tables and Views</span></span></p></td>
  <td><p><span data-ttu-id="42dc4-128">Nombres de tablas específicas de la base de datos</span><span class="sxs-lookup"><span data-stu-id="42dc4-128">Names of specific tables in your database</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="42dc4-129">Fecha de modificación</span><span class="sxs-lookup"><span data-stu-id="42dc4-129">Modified Date</span></span></p></td>
  <td><p><span data-ttu-id="42dc4-130">Hoy; Ayer; Mes pasado; Con más de</span><span class="sxs-lookup"><span data-stu-id="42dc4-130">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="42dc4-131">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="42dc4-131">Created Date</span></span></p></td>
  <td><p><span data-ttu-id="42dc4-132">Hoy; Ayer; El mes pasado; Antiguo</span><span class="sxs-lookup"><span data-stu-id="42dc4-132">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="42dc4-133">Categoría personalizada</span><span class="sxs-lookup"><span data-stu-id="42dc4-133">Custom category</span></span></p></td>
  <td><p><span data-ttu-id="42dc4-134">Nombres de grupos que creó para la categoría personalizada especificada</span><span class="sxs-lookup"><span data-stu-id="42dc4-134">Names of groups you have created for the specified custom category</span></span></p></td>
  </tr>
  </tbody>
  </table>

- <span data-ttu-id="42dc4-135">Para ejecutar la acción **DesplazarseA** en un módulo de VBA, use el método **NavigateTo** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="42dc4-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>

> [!NOTE]
> <span data-ttu-id="42dc4-p105">[!NOTA] Para desplazarse al nivel superior de una categoría (por ejemplo, **Todas las tablas**, **Todos los objetos de Access** o **Todas las fechas**), deje el argumento Grupo en blanco. Por ejemplo, cuando el valor del argumento **Categoría** es **Tipo de objeto** y se especifica **Todos los objetos de Access** como argumento **Grupo**, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="42dc4-p105">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank. For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span></span>


