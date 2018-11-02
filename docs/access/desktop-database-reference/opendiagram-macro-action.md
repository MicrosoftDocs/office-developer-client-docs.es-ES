---
title: AbrirDiagrama (acción de macro)
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c170c9d02967cb04b387d9f549ad77933d1f55b8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925649"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="882b2-102">AbrirDiagrama (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="882b2-102">OpenDiagram macro action</span></span>


<span data-ttu-id="882b2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="882b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="882b2-104">En un proyecto de Access, puede usar la acción **AbrirDiagrama** para abrir un diagrama de base de datos en la vista Diseño.</span><span class="sxs-lookup"><span data-stu-id="882b2-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>


> [!NOTE]
> <P><span data-ttu-id="882b2-p101">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="882b2-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="882b2-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="882b2-107">Setting</span></span>

<span data-ttu-id="882b2-108">La acción **AbrirDiagrama** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="882b2-108">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="882b2-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="882b2-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="882b2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="882b2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="882b2-111"><strong>Nombre de diagrama</strong></span><span class="sxs-lookup"><span data-stu-id="882b2-111"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="882b2-112">El nombre del diagrama de base de datos para abrir.</span><span class="sxs-lookup"><span data-stu-id="882b2-112">The name of the database diagram to open.</span></span> <span data-ttu-id="882b2-113">El cuadro <strong>Nombre de diagrama</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todos los diagramas de base de datos en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="882b2-113">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="882b2-114">Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="882b2-114">This is a required argument.</span></span> <span data-ttu-id="882b2-115">Si ejecuta una macro que contiene la acción <strong>AbrirDiagrama</strong> en una base de datos de biblioteca, Microsoft Access busca primero el diagrama con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="882b2-115">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="882b2-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="882b2-116">Remarks</span></span>

<span data-ttu-id="882b2-117">Esta acción es similar a hacer doble clic en un diagrama de base de datos en el panel de navegación, o bien, a hacer clic con el botón secundario en el diagrama de base de datos en el panel de navegación y después en **Vista Diseño**.</span><span class="sxs-lookup"><span data-stu-id="882b2-117">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>


> [!TIP]
> <P><span data-ttu-id="882b2-p103">[!SUGERENCIA] Puede arrastrar un diagrama de base de datos desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción <STRONG>AbrirDiagrama</STRONG> que abre el diagrama de base de datos en la vista Diseño.</span><span class="sxs-lookup"><span data-stu-id="882b2-p103">You can drag a database diagram from the Navigation Pane to a macro action row. This automatically creates an <STRONG>OpenDiagram</STRONG> action that opens the database diagram in Design view.</span></span></P>



<span data-ttu-id="882b2-120">Para ejecutar la acción **AbrirDiagrama** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenDiagram** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="882b2-120">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

