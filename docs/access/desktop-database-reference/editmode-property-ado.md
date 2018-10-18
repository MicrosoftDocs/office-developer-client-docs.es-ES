---
<<<<<<< Título HEAD: EditMode (propiedad) (ADO) TOCTitle: EditMode (propiedad) (ADO) === título: EditMode (propiedad, ADO) TOCTitle: EditMode (propiedad, ADO)
>>>>>>> Master ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: ms.date 48543867: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="editmode-property-ado"></a>EditMode (propiedad, ADO)
=======
# <a name="editmode-property-ado"></a>EditMode (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el estado de modificación del registro actual.

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve un valor [EditModeEnum](editmodeenum.md).

## <a name="remarks"></a>Comentarios

ADO mantiene un búfer de modificación asociado al registro actual. Esta propiedad indica si se han realizado cambios en este búfer o si se ha creado un registro nuevo. Utilice la propiedad **EditMode** para determinar el estado de modificación del registro actual. Puede probar cambios pendientes si un proceso de modificación se ha interrumpido y determinar si debe utilizar el método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md).

Vea el método [AddNew](addnew-method-ado.md) para obtener una descripción más detallada de la propiedad **EditMode** en condiciones de modificación diferentes.

Cuando una llamada a [Eliminar](delete-method-ado-recordset.md) no elimina correctamente el registro o registros en los datos de origen (debido a, por ejemplo, infracciones de integridad referencial), el [objeto Recordset](recordset-object-ado.md) permanecerá en modo de edición (**EditMode** = **adEditInProgress **). Eso significa que es necesario llamar a **CancelUpdate** antes de quitar el registro actual (con [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) o [Close](close-method-ado.md), por ejemplo).


> [!NOTE]
> <P>[!NOTA] <STRONG>EditMode</STRONG> puede devolver un valor válido únicamente si hay un registro actual. <STRONG>EditMode</STRONG> devolverá un error si <A href="bof-eof-properties-ado.md">BOF o EOF</A> son True o si se ha eliminado el registro actual.</P>


