---
title: Prever errores
TOCTitle: Anticipating Errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f062eb86b45778cc7f25fb2d0d0588b82bdd78b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485942"
---
# <a name="anticipating-errors"></a><span data-ttu-id="af495-102">Prever errores</span><span class="sxs-lookup"><span data-stu-id="af495-102">Anticipating Errors</span></span>


<span data-ttu-id="af495-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="af495-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="af495-p101">La prevención de errores es tan importante como el tratamiento de éstos. Esta última sección contiene una breve lista de medidas de precaución que se pueden adoptar en la aplicación para reducir la probabilidad de que se produzcan errores.</span><span class="sxs-lookup"><span data-stu-id="af495-p101">Error prevention is at least as important as error handling. This final section contains a short list of precautions your application can take to help make errors less likely to occur.</span></span>

<span data-ttu-id="af495-p102">Compruebe el estado de los objetos observando el valor de la propiedad **State** antes de intentar realizar una operación que utilice esos objetos. Por ejemplo, si su aplicación utiliza una **conexión** global, compruebe su propiedad **State** para ver si está abierta antes de llamar al método **Open**.</span><span class="sxs-lookup"><span data-stu-id="af495-p102">Check the state of objects by checking the value in the **State** property before trying to perform an operation using those objects. For example, if your application uses a global **Connection**, check its **State** property to see if it is already open before calling the **Open** method.</span></span>

  - <span data-ttu-id="af495-p103">Cualquier programa que acepte datos de un usuario debe incluir código para validar esos datos antes de enviarlos al almacén de datos. No puede confiar en que el almacén de datos, ni el proveedor, ni ADO, y ni siquiera el lenguaje de programación, le notificarán los problemas. Debe revisar cada byte que introduzcan los usuarios y comprobar que los datos son del tipo correcto para el campo correspondiente y que los campos obligatorios no están vacíos.</span><span class="sxs-lookup"><span data-stu-id="af495-p103">Any program that accepts data from a user must include code to validate that data before sending it to the data store. You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems. You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</span></span>

<span data-ttu-id="af495-p104">Compruebe los datos antes de intentar escribirlos en el almacén de datos. La forma más sencilla de hacerlo es controlar los eventos **WillMove** o **WillUpdateRecordset**. Para obtener una descripción más completa de cómo controlar los eventos de ADO, vea [Capítulo 7: Controlar eventos de ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="af495-p104">Check the data before you try to write any data to the data store. The easiest way to do so is to handle the **WillMove** event or the **WillUpdateRecordset** event. For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

<span data-ttu-id="af495-p105">Asegúrese de que los objetos **Recordset** no se salen de los límites del **conjunto de registros** antes de intentar mover el puntero de registros. Si trata de **desplazarse al siguiente** cuando **EOF** es True o **desplazarse al anterior** cuando **BOF** es True, se producirá un error. Si ejecuta cualquiera de los métodos **Move** cuando tanto **EOF** como **BOF** son True, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="af495-p105">Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer. If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur. If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.</span></span>

<span data-ttu-id="af495-117">También se producirán errores si intenta realizar operaciones como **Seek** y **Find** en un **conjunto de registros** vacío.</span><span class="sxs-lookup"><span data-stu-id="af495-117">Errors also will occur if you try to perform operations such as **Seek** and **Find** on an empty **Recordset**.</span></span>

