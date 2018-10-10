---
title: BuscarRegistroSiguiente (acción de macro)
TOCTitle: FindNextRecord Macro Action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b58478a67468fa7d00c348066459672bc31c52a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485917"
---
# <a name="findnextrecord-macro-action"></a><span data-ttu-id="f17f0-102">BuscarRegistroSiguiente (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="f17f0-102">FindNextRecord Macro Action</span></span>


<span data-ttu-id="f17f0-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f17f0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f17f0-p101">Puede usar la acción **BuscarRegistroSiguiente** para buscar el siguiente registro que cumpla los criterios especificados por la anterior acción **BuscarRegistro** o el valor en el cuadro de diálogo **Buscar y reemplazar** (en la ficha **Inicio**, haga clic en **Buscar**). Puede usar la acción **BuscarRegistroSiguiente** para buscar registros repetidamente. Por ejemplo, para recorrer sucesivamente todos los registros de un cliente concreto.</span><span class="sxs-lookup"><span data-stu-id="f17f0-p101">You can use the **FindNextRecord** action to find the next record that meets the criteria specified by the previous **FindRecord** action or the value in the **Find and Replace** dialog box (on the **Home** tab, click **Find**). You can use the **FindNextRecord** action to search repeatedly for records. For example, you can move successively through all the records for a specific customer.</span></span>

## <a name="setting"></a><span data-ttu-id="f17f0-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="f17f0-107">Setting</span></span>

<span data-ttu-id="f17f0-p102">La acción **BuscarRegistroSiguiente** no tiene argumentos. La acción **BuscarRegistroSiguiente** busca el siguiente registro que cumpla los criterios establecidos por la acción **BuscarRegistro** o en el cuadro de diálogo **Buscar y reemplazar**. Los argumentos de la acción **BuscarRegistro** se comparten con las opciones del cuadro de diálogo **Buscar y reemplazar**.</span><span class="sxs-lookup"><span data-stu-id="f17f0-p102">The **FindNextRecord** action doesn't have any arguments. The **FindNextRecord** action finds the next record that meets the criteria set either by the **FindRecord** action or in the **Find and Replace** dialog box. The arguments for the **FindRecord** action are shared with the options in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="f17f0-p103">Para establecer los criterios de búsqueda, utilice la acción **BuscarRegistro**. Normalmente, se inserta una acción **BuscarRegistro** en una macro y, a continuación, se utiliza la acción **BuscarRegistroSiguiente** para buscar los registros subsiguientes que cumplan los mismos criterios. Para buscar registros sólo cuando se cumple una condición concreta, se puede incluir una expresión condicional en la columna **Condición** de la fila correspondiente a la acción **BuscarRegistroSiguiente**.</span><span class="sxs-lookup"><span data-stu-id="f17f0-p103">To set the search criteria, use the **FindRecord** action. Typically, you enter a **FindRecord** action in a macro and then use the **FindNextRecord** action to find succeeding records that meet the same criteria. To search for records only when a certain condition is met, you can enter a conditional expression in the **Condition** column of the action row for the **FindNextRecord** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="f17f0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f17f0-114">Remarks</span></span>

<span data-ttu-id="f17f0-115">Esta acción tiene el mismo efecto que utilizar el botón **Buscar siguiente** del cuadro de diálogo **Buscar y reemplazar**.</span><span class="sxs-lookup"><span data-stu-id="f17f0-115">This action has the same effect as using the **Find Next** button in the **Find and Replace** dialog box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f17f0-p104">[!NOTA] Si bien la acción <STRONG>BuscarRegistro</STRONG> corresponde al comando <STRONG>Buscar</STRONG> en la ficha <STRONG>Inicio</STRONG> de tablas, consultas y formularios, no corresponde al comando <STRONG>Buscar</STRONG> del menú <STRONG>Edición</STRONG> en la ventana Código. No se puede utilizar la acción <STRONG>BuscarRegistro</STRONG> o <STRONG>BuscarRegistroSiguiente</STRONG> para buscar texto en módulos.</span><span class="sxs-lookup"><span data-stu-id="f17f0-p104">Although the <STRONG>FindRecord</STRONG> action corresponds to the <STRONG>Find</STRONG> command on the <STRONG>Home</STRONG> tab for tables, queries, and forms, it doesn't correspond to the <STRONG>Find</STRONG> command on the <STRONG>Edit</STRONG> menu in the Code window. You can't use the <STRONG>FindRecord</STRONG> action or <STRONG>FindNextRecord</STRONG> action to search for text in modules.</span></span></P>




> [!TIP]
> <P><span data-ttu-id="f17f0-118">[!SUGERENCIA] Si ha establecido en <STRONG>Sí</STRONG> el valor del argumento <STRONG>Sólo el campo activo</STRONG> de la acción <STRONG>BuscarRegistro</STRONG>, es posible que tenga que utilizar la acción <STRONG>IrAControl</STRONG> para mover el enfoque al control que contiene los datos que está buscando antes de utilizar la acción <STRONG>BuscarRegistroSiguiente</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f17f0-118">If you've set the <STRONG>Only Current Field</STRONG> argument of the <STRONG>FindRecord</STRONG> action to <STRONG>Yes</STRONG>, you may need to use the <STRONG>GoToControl</STRONG> action to move the focus to the control containing the data you're searching for before you use the <STRONG>FindNextRecord</STRONG> action.</span></span></P>



<span data-ttu-id="f17f0-p105">Si el texto seleccionado actualmente es el mismo que el texto seleccionado en el momento en el que se ejecuta la acción de macro **BuscarRegistroSiguiente**, la búsqueda se inicia inmediatamente después de la selección, en el mismo campo que la selección y en el mismo registro. En caso contrario, la búsqueda se inicia al principio del registro activo. Esto permite buscar múltiples instancias de los mismos criterios de búsqueda que pudieran aparecer en un único registro.</span><span class="sxs-lookup"><span data-stu-id="f17f0-p105">If the currently selected text is the same as the search text at the time the **FindNextRecord** macro action is carried out, the search begins immediately following the selection, in the same field as the selection, and in the same record. Otherwise, the search begins at the start of the current record. This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="f17f0-p106">Sin embargo, observe que si usa un botón de comando para ejecutar una macro que contenga la acción **BuscarRegistroSiguiente**, se buscará de forma repetida la primera instancia de los criterios de búsqueda. Este comportamiento se debe a que, al hacer clic en el botón de comando, se quita el enfoque del campo que contiene el valor coincidente. La acción **BuscarRegistroSiguiente** empezará la búsqueda desde el principio del registro. Para evitar este problema, ejecute la macro usando una técnica que no cambie el enfoque, como un botón de una barra de herramientas personalizada o una combinación de teclas definida en una macro AutoKeys. Asimismo, establezca el enfoque de la macro en el campo que contiene los criterios de búsqueda antes de llevar a cabo la acción **BuscarRegistroSiguiente**.</span><span class="sxs-lookup"><span data-stu-id="f17f0-p106">However, note that if you use a command button to run a macro containing the **FindNextRecord** action, the first instance of the search criteria will be found repeatedly. This behavior occurs because clicking the command button removes the focus from the field containing the matching value. The **FindNextRecord** action will then begin searching from the start of the record. To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro. Alternatively, set the focus in the macro to the field containing the search criteria before you carry out the **FindNextRecord** action.</span></span>

<span data-ttu-id="f17f0-127">Se produce el mismo comportamiento si se utiliza un botón de comando para ejecutar una macro que contenga la acción **BuscarRegistro** con el argumento **Buscar primero** establecido en **No**.</span><span class="sxs-lookup"><span data-stu-id="f17f0-127">The same behavior also occurs if you use a command button to run a macro containing the **FindRecord** action with the **Find First** argument set to **No**.</span></span>

<span data-ttu-id="f17f0-128">Para ejecutar la acción **BuscarRegistroSiguiente** desde un módulo de Visual Basic para Aplicaciones, use el método **FindNext** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="f17f0-128">To run the **FindNextRecord** action in a Visual Basic for Applications module, use the **FindNext** method of the **DoCmd** object.</span></span>

