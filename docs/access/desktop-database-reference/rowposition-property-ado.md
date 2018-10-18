---
<<<<<<< Título HEAD: RowPosition (propiedad) (ADO) TOCTitle: RowPosition (propiedad) (ADO) === título: RowPosition (propiedad, ADO) TOCTitle: RowPosition (propiedad, ADO)
>>>>>>> Master ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: ms.date 48547325: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="rowposition-property-ado"></a>RowPosition (propiedad, ADO)
=======
# <a name="rowposition-property-ado"></a>RowPosition (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013



Obtiene o establece un objeto **RowPosition** de OLE DB desde o en un objeto **ADORecordsetConstruction**. Al usar **colocar\_RowPosition** para establecer el objeto **RowPosition** , el objeto **Recordset** resultante utiliza el objeto **RowPosition** para determinar la fila actual.

Lectura y escritura.

## <a name="syntax"></a>Sintaxis

Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos);

Poner HRESULT\_RowPosition (\[en\] IUnknown\* pRowPos);

## <a name="parameters"></a>Parámetros

  - *ppRowPos*

  - Puntero a un objeto **RowPosition** de OLE DB.

  - *PRowPos*

  - Un objeto **RowPosition** de OLE DB.

<<<<<<< HEAD
## <a name="return-values"></a>Valores devueltos
=======
## <a name="return-values"></a>Valores devueltos
>>>>>>> master

Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.

## <a name="remarks"></a>Comentarios

Cuando se establece esta propiedad, si el objeto **Rowset** del objeto **RowPosition** es diferente al objeto **Rowset** del objeto **Recordset**, el primero sobrescribe al segundo. El mismo comportamiento se aplica al **capítulo** actual de **RowPosition**.

## <a name="applies-to"></a>Se aplica a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

