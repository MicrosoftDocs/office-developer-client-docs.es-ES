---
<span data-ttu-id="646f4-101"><<<<<<< Título HEAD: marcador (propiedad) (ADO) TOCTitle: marcador (propiedad) (ADO) === título: Bookmark (propiedad, ADO) TOCTitle: Bookmark (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="646f4-101"><<<<<<< HEAD title: Bookmark Property (ADO) TOCTitle: Bookmark Property (ADO) ======= title: Bookmark property (ADO) TOCTitle: Bookmark property (ADO)</span></span>
>>>>>>> <span data-ttu-id="646f4-102">Master ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15) ms:contentKeyID: ms.date 48543287: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="646f4-102">master ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15) ms:contentKeyID: 48543287 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="646f4-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="646f4-103"><<<<<<< HEAD</span></span>
# <a name="bookmark-property-ado"></a><span data-ttu-id="646f4-104">Bookmark (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="646f4-104">Bookmark Property (ADO)</span></span>
=======
# <a name="bookmark-property-ado"></a><span data-ttu-id="646f4-105">Bookmark (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="646f4-105">Bookmark property (ADO)</span></span>
>>>>>>> <span data-ttu-id="646f4-106">master</span><span class="sxs-lookup"><span data-stu-id="646f4-106">master</span></span>


<span data-ttu-id="646f4-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="646f4-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="646f4-108">Indica un marcador que identifica de manera única el registro actual de un objeto [Recordset](recordset-object-ado.md) o que establece el registro actual de un objeto **Recordset** en el registro identificado por un marcador válido.</span><span class="sxs-lookup"><span data-stu-id="646f4-108">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

<span data-ttu-id="646f4-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="646f4-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="646f4-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="646f4-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="646f4-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="646f4-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="646f4-112">master</span><span class="sxs-lookup"><span data-stu-id="646f4-112">master</span></span>

<span data-ttu-id="646f4-113">Establece o devuelve una expresión de tipo **Variant** que da como resultado un marcador válido.</span><span class="sxs-lookup"><span data-stu-id="646f4-113">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="646f4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="646f4-114">Remarks</span></span>

<span data-ttu-id="646f4-p101">Utilice la propiedad **Bookmark** para guardar la posición del actual registro y volver al mismo más adelante. Los marcadores sólo están disponibles en los objetos **Recordset** que admitan la funcionalidad de los marcadores.</span><span class="sxs-lookup"><span data-stu-id="646f4-p101">Use the **Bookmark** property to save the position of the current record and return to that record at any time. Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="646f4-p102">Al abrirse un objeto **Recordset**, cada uno de sus registros tiene un marcador único. Para guardar el marcador del registro actual, asigne el valor de la propiedad **Bookmark** a una variable. Para poder volver rápidamente a ese registro después de moverse a otro, establezca la propiedad **Bookmark** del objeto **Recordset** en el valor de dicha variable.</span><span class="sxs-lookup"><span data-stu-id="646f4-p102">When you open a **Recordset** object, each of its records has a unique bookmark. To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="646f4-p103">Puede que el usuario no vea el valor del marcador. Además, los marcadores no son necesariamente comparables de manera directa: dos marcadores que hacen referencia al mismo registro pueden tener valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="646f4-p103">The user may not be able to view the value of the bookmark. Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="646f4-p104">Si se utiliza el método [Clone](clone-method-ado.md) para crear una copia de un objeto **Recordset**, los valores de configuración de la propiedad **Bookmark** de los objetos **Recordset** original y duplicado son idénticos y se pueden utilizar de manera intercambiable. Sin embargo, no se pueden utilizar de manera intercambiable los marcadores de diferentes objetos **Recordset**, incluso si se crearon a partir del mismo origen o comando.</span><span class="sxs-lookup"><span data-stu-id="646f4-p104">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably. However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="646f4-124">**Uso de servicio de datos remotos** Cuando se usa en un objeto **Recordset** de cliente, la propiedad **Bookmark** siempre está disponible.</span><span class="sxs-lookup"><span data-stu-id="646f4-124">**Remote Data Service Usage**When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

